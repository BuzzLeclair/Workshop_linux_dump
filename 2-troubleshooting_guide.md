# Dual Boot Troubleshooting Guide

Comprehensive solutions for common dual boot problems.

---

## Can't Disable Secure Boot

**Symptoms:**
- BIOS shows Secure Boot disabled
- But still reports enabled after restart
- Or BIOS won't allow disabling

**Solution:**

1. **Check BIOS Access Password:**
   - Some systems require password to modify BIOS
   - If you set one, clear it first:
     - BIOS → Security → Clear password

2. **Check Windows Fast Startup:**
   - MUST disable Fast Startup BEFORE touching BIOS
   - Settings → System → Power & sleep
   - Additional power settings → Choose what power button does
   - Change settings that are currently unavailable
   - Uncheck "Turn on fast startup"
   - Click Save changes

3. **Try UEFI Firmware Settings:**
   - Settings → System → About
   - Advanced startup options → Restart now
   - Troubleshoot → UEFI Firmware Settings
   - Disable Secure Boot there

4. **Reset BIOS to Defaults:**
   - BIOS → Settings → Reset to defaults
   - Secure Boot usually defaults to OFF
   - Then save and exit

---

## Can't Boot into BIOS

**Symptoms:**
- Boot menu key not working
- F12/F2/DEL not responding
- Boots straight to Windows

**Solution:**

1. **Shut down completely:**
   - Not sleep or hibernation
   - Right-click Start → Shut down
   - Wait 10 seconds before restarting

2. **Try different boot key:**
   - Try all possibilities: F2, F8, F10, F12, DEL, ESC
   - Press repeatedly during boot

3. **Use Windows Recovery:**
   - Settings → System → About → Advanced options
   - Recovery options → Restart now (under Advanced startup)
   - Select "Troubleshoot"
   - "UEFI Firmware Settings"
   - This boots into BIOS directly

4. **Check USB drive:**
   - Insert USB drive first
   - Boot key might be different with USB present
   - Often F12 or ESC with USB

5. **Try USB boot directly:**
   - Power off and insert USB
   - Power on
   - If booting to Windows still, try forcing boot menu again

---

## Installer Asks for WiFi but Network Unavailable

**Symptoms:**
- Installer asks for WiFi connection
- But no networks showing
- Can't proceed

**Solution:**

* **Skip network for now:**
   - Many installers allow skipping
   - Continue without internet
   - Install network drivers after

* **Restart and try again:**
   - Go back to USB menu
   - Restart installer
   - Sometimes WiFi is detected on retry

* **Update BIOS WiFi driver:**
   - May need updated driver first
   - Use USB tethering from phone:
     - Connect phone with USB
     - Enable USB tethering in phone settings
     - Use phone internet for installation


## System Time Wrong (Windows Shows Different Time After Boot)

**Symptoms:**
- Boot Windows, time is correct
- Boot Linux, time changes
- Or vice versa
- Clock shows wrong time

**Solution:**

1. **Configure Linux UTC:**
   - Linux usually uses UTC
   - Windows uses local time
   - Configure one to match other

   **Set Linux to local time:**
   ```bash
   sudo timedatectl set-local-rtc 1
   sudo systemctl restart systemd-timedated
   ```

   **Set Linux to UTC (recommended):**
   ```bash
   sudo timedatectl set-local-rtc 0
   sudo timedatectl set-ntp true
   ```

2. **Set Windows to UTC:**
   - Windows Registry (advanced):
     - Regedit
     - Computer\\HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\TimeZoneInformation
     - Create DWORD: RealTimeIsUTC
     - Set to 1
     - Restart

3. **Just set time manually:**
   - Each OS individually sets time
   - Not ideal but temporary workaround
