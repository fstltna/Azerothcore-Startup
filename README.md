# AzerothCore Startup Scripts (1.0.0)
Startup scripts for the AzerothCore software - uses the "screen" command to manage a session. This also restarts the AzerothCore processes if it crashes.

---
These start up the AzerothCore server at boot time with a "screen" process.

1. Copy **azerothcore** into **/home/wowowner/bin** - make sure it is executable
2. Copy **startazerothworld** into **/home/wowowner/azerothcore** - make sure it is executable
3. Copy **startazerothauth** into **/home/wowowner/azerothcore** - make sure it is executable
4. Put **@reboot /home/wowowner/bin/azerothcore start** into your crontab

When you want to view the AzerothCore console, just enter "**screen -r**" in your shell.

To disconnect from the AzerothCore console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 24.04 server...

If you want to turn off the server respawning type "**touch /home/wowowner/azerothcore/nostart**". To reenable it type "**rm /home/wowowner/azerothcore/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
