# squeezelite-ds214
startup script for squeezelite on ds214ply
If you run a logitech media server on a synology diskstation and have USB sound connected 
it would also be nice to play directly from the logitech server to the local USB sound card.
As there seem to be no ready to go solution I tried using squeezelite -https://code.google.com/archive/p/squeezelite/downloads.
Fortunately on a DS214play (atom) based, the Squeezelite 1.5 Linux ALSA Intel 32 bit binary runs.
You have to install some ipkg before - for set up instructions refer to http://www.synology-wiki.de/index.php/IPKG.
You need to install:
ipkg install alsa-tools
ipkg install mp123
Afterwards copy (as root) the binary to /opt/bin and download the S99squeezelite to /opt/etc/init.d.
Make it mode 755 as root.
You can start it using /opt/etc/init.d/S99squeezelite start.
Your logitech server should display a ds214 play entry.
If necessary you can adapt the name inside the script or tune the output and buffering parameters.
