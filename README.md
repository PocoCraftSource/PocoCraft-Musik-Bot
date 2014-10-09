PocoCraft-Musik-Bot
===================

This is the "PocoCraft Musik Bot" core API that everybody kept asking me about, so here it is!

You will need to manually install the TeamSpeak 3 server and client onto your server/machine in order to correctly start this application as intended(http://www.teamspeak.com/?page=downloads).

For now you will need to manually configure PulseAudio so that VLC(default media player) will output to a default recording device(soon this will be changed upon installation).
You can configure this by using Paprefs and Pavucontrol until it is implemented.

Prerequisites: dos2unix, vlc, pulseaudio, bash, netcat
Recommends: paprefs, pavucontrol

How to install prerequisites using a terminal: sudo apt-get install dos2unix vlc pulseaudio bash netcat
How to install recommends using a terminal: sudo apt-get install paprefs pavucontrol

You will need to manually edit the configuration file in /etc/pococraft/pococraft-scripts.conf
The main variables that will probably need to be changed for your setup are: VLCMEDIAPLAYERMUSICDIRECTORY, CURRENTCLIDIDTEMPFILE, TEAMSPEAKINSTALLATIONUSERNAME, TEAMSPEAKCLIENTINSTALLATIONDIRECTORY, TEAMSPEAKSERVERINSTALLATIONDIRECTORY, TEAMSPEAKCLIENTBINARYFILENAME

If you have paprefs installed you can enable other advanced settings such as network streaming.
If you have Pavucontrol you can make the recording from device default(in my case "Monitor of RTP Multicast Sink") by checking the green checkmark(set as fallback), then you will need to make TeamSpeak3 listen on that device by telling it to use the default PulseAudio device(Settings > Options > Capture > Capture Device > Default) using the PulseAudio Capture Mode.
