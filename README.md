# Welcome to the wonderful world of linux !!
![yay !!](image-1.png)


First, disable bitlocker : execute `manage-bde -status` to see if it is active

If it is, disable it : `manage-bde -off`

# If you want a dual boot : (you can ignore if you want to remove windows entirely)

**Check disk space:**
- Windows: Right-click C:\ → Properties → Note free space
- Minimum required: **50GB free disk space**

if you dont have enough space, download https://diskanalyzer.com/ and remove useless folders (games usually) (the visualizer helps a lot !)

Then shrink your C:\ partition of your disk using : https://www.partitionwizard.com/

# When in the installer

If you still want a dual boot : select "install alongside windows"

if you want to wipe your drive and only have linux on it, select "use entire disk"

## BIOS/UEFI : Disable Features

Before the workshop, disable these in BIOS/UEFI:

- **Secure Boot** (disable in bios)

### Step 3: Prepare for Installation

- Enable USB boot (usually enabled by default)
- Check boot order options

---

## Documentation & Notes

- If you do not have windows activated, https://github.com/massgravel/Microsoft-Activation-Scripts

---

## USB drive not detected?
- Try a different USB port

## BIOS won't boot from USB?
- Enable "USB Boot" in BIOS

## Still having issues?
- Bring laptop to workshop early for pre-workshop help
- Ask for help from the goat Romain

---

## Congratulations!

Congrats, now you can attend the other workshop (about bash scripting :] )

Now you can add other software I personnally use to use linux as a daily OS
- Teams for linux, pretty understandable https://github.com/IsmaelMartinez/teams-for-linux
- vesktop, (an opensource discord port with vencord (like betterdiscord) https://github.com/Vencord/Vesktop
- VScode https://code.visualstudio.com/docs/setup/linux

- You can also change your desktop environnement. Fedora's default is Gnome, but I use KDE. (you can just search for those yourself, there are a lot !)


![yay !!](image.png)