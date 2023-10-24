# Retroflag GPi CASE 2 - Recalbox scripts
Helper scripts for Retroflag GPI CASE 2 running Recalbox

## Save before shutdown script
This script will save the current game and stops the emulator (RetroArch) before the system powers off.
So no more accidential loss of the game state. ;-)
 
### Installation
1. 	connect with ssh to your recallbox (ip can befound in the main menu -> network settings) e.g. ssh root@192.168.1.10
 		default password: `recalboxroot` 

2. 	remount filesystem for writing:
		`mount -o remount, rw /`

3. 	create new file
		`vim /etc/init.d/S99_custom_save_before_shutdown`

4.	insert the whole content of the file `S99_custom_save_before_shutdown` inside this repository

5.	save and exit file

6. 	make file executable
		`chmod 755 /etc/init.d/S99_custom_save_before_shutdown`

7. 	ENJOY! ;-)

### Test info
Tested on Retroflag GPi CASE 2 with Raspberry Pi Compute Module 4, 4GB RAM, Lite.
OS: Recalbox 9.1


# Additional links to the docs used in the scripts
- RetroArch Network Control Interface documentation: https://docs.libretro.com/development/retroarch/network-control-interface/
- Login via SSH to Recalbox: https://wiki.recalbox.com/en/tutorials/system/access/root-access-terminal-cli
