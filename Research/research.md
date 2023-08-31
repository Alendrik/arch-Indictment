# Alendrik Research
## Overview
**Research Goal**: Identify best starting points within arch and lay out a roadmap to follow generally.
- Probably using arch for the sole purpose of saying that we're using it.
- Generate a roadmap

**Guiding Questions**: (These questions are just a rough idea of what I'm trying to get at. Not a template)
- What should I know?
- What do I need?
- Where Do I get it?
- What Dependencies do I need pre-install
- Once installed... what now?
- What are the major considerations to take into account
	- Tile manager/window manager vs Desktop Env.
	- dependencies
	- etc.


## Step 0 - Preparation
### What Should I Know
	What do I need to start? HW reqs? Any concerns over different firmware/HW/middleware/etc? Can I just plug in my USB stick and have the rest work (that's what she said).
	
	Some things worth noting are partition schemes, pacman familiarization, and post-installation processes. There are also plenty of other things within the wiki repository and AUR. 

- **partition schemes**: sometimes, a /home partition is made (and generally recommended).
	- [insert reason]
- **Pacman Familiarization**: Arch's package manager. Important to learn intricacies and relation to AUR. 
	- AUR, [explain intricacies]
- **Post-Installation Processes**: 
	- Setting up the bootloader
	- Installing drivers and other necessary devices

### What Do I Need
	There will be some things that are important/highly recommended.
- Ethernet highly recommended.
	- wifi-menu (ncurses configuration)
	- iwctl (another Wi-Fi option)
- Pick important backup options. (timeshift, betterfs)
- Pick appropriate Kernel to the machine. (will have impacts on what we do looking forward)
- Understand BIOS vs UEFI installation.
	- Good Partitioning Guide (Denshi comfy install)
	- 


### What NOT to do
	There are certain things that should be avoided within arch specifically for stability.
- Do NOT update everyday. (weekly)
- Do NOT install out-of-date packages. (check AUR for "flagged as out-of-date")
- Do NOT forget to assign excess memory partiion. (else crash)








## Un-Organized Notes
Find a functional kernel version and stick to it.
Read the Wiki...... yeah....
> pacman -Syy (sync to mirror)
> timedatectl set-ntp true
> loadkeys (lang)

Show all devices attached
> lsblk

Certain things should not be auto-updated. Consider adding ignore package entries to pacman/conf file. 
> sudo vim /etc/pacman/conf

While the wiki recommends using fdisk to partition. cfdisk is recommened and more intuitive.
> cfdisk (follow the prompts)

New System + 2TB disk size = gpt (dos will break at larger disk sizes)
Older Sys  + <2TB = Dos 

Formatting as ext4
> mkfs.ext4 [partition name]



- We will **NOT** be using archinstall, BUT we can learn lots about what it is doing in the background. YT easy arch install. 
	- Notables:
	- Bootloader 
		- GRB vs systemd-boot: Grub is less bloated
	- User setup (hostname, PW, users, profile)
	- Mirror Regions
	- swap?
	- Kernels
	- network configuration
	- timezone (timesync NTP?)
	- Addtional packages/repos?
	- Which Partition? FS to go along with it?
	- Audio Drivers




## Resources Used
- https://wiki.archlinux.org/title/Window_manager
- https://wiki.archlinux.org/title/Comparison_of_tiling_window_managers
- https://www.techjunkie.com/tiling-window-managers/
- YT archinstall (Mental Outlaw)
- How to make Arch Linux Stable -- Christ Titus Tech
- Comfy install guide -- DenshiVideo 
- Arch install -- mental outlaw
