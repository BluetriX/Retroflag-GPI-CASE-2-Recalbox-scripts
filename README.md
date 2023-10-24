# Retroflag GPi CASE 2 - Recalbox scripts
Helper scripts for Retroflag GPI CASE 2 running Recalbox

## Save before shutdown script
This script will save the current game and stops the emulator (RetroArch,  e.g. GameBoyColor) before the system powers off.
So no more accidential loss of the game state. ;-)
 
### Installation
1.  connect with ssh to your recallbox (ip can befound in the main menu -> network settings) e.g. ssh root@192.168.1.10
   
    default password: `recalboxroot` 

2. 	remount filesystem for writing:

	`mount -o remount, rw /`

3. 	create new file
   
	`vim /etc/init.d/S99_custom_save_before_shutdown`

4.	insert the whole content of the file `S99_custom_save_before_shutdown` inside this repository

5.	save and exit file

6. 	make file executable
    
	`chmod 755 /etc/init.d/S99_custom_save_before_shutdown`
7.	reboot

8. ENJOY! ;-)

### Uninstall
1. connect with ssh to your recallbox
2. remount filesystem for writing: `mount -o remount, rw /
3. rm /etc/init.d/S99_custom_save_before_shutdown
4. reboot

## Autosave script
This script will save the current game (RetroArch, e.g. GameBoyColor) every 300 seconds (5 minutes).
So no more accidential loss of the game state. ;-)

Warning: Setting the autosave interval value too low will cause all sorts of issue, most notably hardware degradation.
 
### Installation
1. 	connect with ssh to your recallbox (ip can befound in the main menu -> network settings) e.g. ssh root@192.168.1.10

   	default password: `recalboxroot` 

2. 	remount filesystem for writing:
	
     `mount -o remount, rw /`

3. 	create new file
	
     `vim /etc/init.d/S99_custom_autosave_300s`

4.	insert the whole content of the file `S99_custom_autosave_300s` inside this repository

5.	save and exit file

6. 	make file executable
	
     `chmod 755 /etc/init.d/S99_custom_autosave_300s`
7.	reboot

8. 	ENJOY! ;-)

### Uninstall
1. connect with ssh to your recallbox
2. remount filesystem for writing: `mount -o remount, rw /
3. rm /etc/init.d/S99_custom_autosave_300s
4. reboot

# Test info
Tested on the following System:
* Retroflag GPi CASE 2 with Raspberry Pi Compute Module 4, 4GB RAM, Lite.
* OS: Recalbox 9.1
* Emulator: GameBoyColor (RetroArch)


# Additional links to the docs used in the scripts
- RetroArch Network Control Interface documentation: https://docs.libretro.com/development/retroarch/network-control-interface/
- Login via SSH to Recalbox: https://wiki.recalbox.com/en/tutorials/system/access/root-access-terminal-cli
