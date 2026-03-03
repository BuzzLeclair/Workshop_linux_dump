# Pre-Workshop Checklist

Complete this checklist before attending the dual boot workshop. 

---

**Check disk space:**
- Windows: Right-click C:\ → Properties → Note free space
- Minimum required: **30GB free disk space**

## BIOS/UEFI Configuration

### Step 1: Check Your Current Setup

- [ ] **Check if you have UEFI or BIOS:**
  - Windows 10/11: Settings → System → About → Scroll to "System firmware" 
  - Note down: UEFI or BIOS
  
- [ ] **Check current boot mode:**
  - Windows: Run `msinfo32` → look for "BIOS Mode"
  - Note down: UEFI or Legacy

### Step 2: Disable Features

First, disable the bitlocker : execute `manage-bde -status` to see if it is active

If it is, disable it : `manage-bde -off`

Before the workshop, disable these in BIOS/UEFI:

- [ ] **Secure Boot** (disable)
- [ ] **Fast Startup** (disable in Windows)
  - Settings → System → Power & sleep → Additional power settings → Choose what the power button does → Change settings that are currently unavailable → Uncheck "Turn on fast startup"

### Step 3: Prepare for Installation

- [ ] Enable USB boot (usually enabled by default)
- [ ] Check boot order options

---

## Create Installation Media

### Download ISO Files

Choose ONE Linux distribution and download its ISO:

- [ ] **Ubuntu 24.04 LTS** (Recommended for beginners)
  - https://ubuntu.com/download/desktop
  - Size: ~4.5GB

- [ ] **Fedora 41** (Best for developers)
  - https://getfedora.org/en/workstation/download/
  - Size: ~2.0GB

- [ ] **Pop!_OS 24.04** (Great desktop experience)
  - https://pop.system76.com/
  - Size: ~3.5GB

- [ ] **Litteraly any other distibution, there are dozens**
  - Find them yourself

### Create Bootable USB Drive


**: Windows 11 Built-in Tool**
- [ ] Right-click ISO file → Mount
- [ ] Windows 11 has built-in USB writer

**: Rufus (preferred)**
- [ ] Download Rufus: https://rufus.ie/
- [ ] Follow steps on the tool 

---

## Documentation & Notes

### Before Workshop Day

- [ ] Write down Windows product key (if you have it)
- [ ] If you do not have windows installed, https://github.com/massgravel/Microsoft-Activation-Scripts

### Choose Your Distribution

- [ ] **Ubuntu**
- [ ] **Fedora**
- [ ] **Pop!_OS**
- [ ] **Any other distribution you found on TikTok**

---

## Troubleshooting Before Workshop

### Can't download the ISO?
- Try a different mirror
- Use a different network

### USB drive not detected?
- Try a different USB port

### BIOS won't boot from USB?
- Enable "USB Boot" in BIOS

### Still having issues?
- Bring laptop to workshop early for pre-workshop help
- Ask for help from the goat Romain

---

## You're Ready!
