Starting with just a copy of the redit post that started it all. 

https://www.reddit.com/r/HearthDisplay/comments/16o797p/hearth_display_hacking/?rdt=35402

Disclamer, I am not a hardware developer, I have not used android in almost 10 years, i don't even use linux regularly, and I am a brute force developer. My day job is devops/system adminstration. If you follow any of these guides below you can see what I am resposible for at https://unlicense.org/


Just for reference; I did all of this because the company wants me to spend 10 dollars a month for weather. Nah. I’ve gotten rid of services for less. Let’s get this party started.

Successfully removed the hearth apps on the device and opened chrome through ADB. It’s not much but it’s an honest living. If anyone has any idea how to get a launcher to work let me know please. I cannot use any I’ve found.
Edit: stock ones didn’t work but nova apparently does. If anyone wants to get to this point. Enable usb debugging by going into settings and connect to ADB shell. Then run TOP to get running services and kill everything that has hearth in the name and there’s also a weird named service on first boot for registration that you need to kill as well. Uninstall of these programs and you are good.
Edit1.5: Google play services and Google store refuse to work right now to get my old nova license so I’m gonna take a back seat on that and work on root because I need to get a full settings menu back.
Edit2: got my old android modding hat back on after about 10 years and worked on it a little bit more yesterday. looks like Android had a partial root already installed on the system and I was able to ADB root into shell so that’s good. Looking to figure out how to modify that to get full root because when I use magisk it complains that root already exists but I can’t do anything else with a locked bootloader yet. Problem is I don’t really have an img file and don’t really wanna brick this board because there is no drop in replacement that I’ve been able to find.
If anyone wants to look for a board the supplier that hearth got all of their smart boards fully assembled is called SHENZHEN ELECTRON TECHNOLOGY CO.,LTD. Found this through the government disclosures that are on sites like “made in China” etc.
You can also see the FCC filing for the internals here: https://fcc.report/FCC-ID/2A896-E0027/6304827.pdf
TL/DR for those of you who don’t wanna read and do the schematics. RockChip rk3568 board with 2gb of ram that has daughter boards connected to:

usb header digitizer
mic
for some reason a usb/ethernet hub
button outputs. 

There might be one im missing but for right now before I release this on github this is like the pre alpha documentation.
I got a pretty good idea about all of the wiring as well so I will likely release an internal schematic if someone wants to do any hardware modding. Seriously considered doing a Pi enabled one because the hardware specs are honestly just bad for anything made in the last 5 years.
To sum it all up: As of 2/3/25 RnD for hardware is complete with full list of components Hearth software removed from the device Launcher installed Open source webpage that does everything hearth does plus weather deployed (from my local home server). Removed hearth from reaching outside off my network.
Going to move this to a GitHub repository soon because I will more than likely do all of this over again and document the process from start to finish.
Edit3: Dumped all of the images for backup. Ready to start the fun.
Edit4: welp she’s toast. Not the hardware or anything but the system image I made as a backup did not get backed up properly by any means and I can’t get it to boot up in stock OS terms. I was able originally to get a full root on it and install a few apps before I wanted to go further.
I ended up buying a converter for the monitor to plug it into a hdmi port and have the touch screen header attach to a usb so I’m gonna toss a raspberry pi on it and call it a day after I install magic mirror and a few other things I needed to have as off server backups. 120 in parts to unlock this thing to use it how I will use it I call it a years worth of hearth subscription saved. If anyone has any questions or wants to send me a recovery image DM me. It was fun!
Edit 5: I got bored over the last couple of days and ended up creating a custom firmware while the part was still shipping from China so I guess I don’t need that or the pi anymore. Unless someone wants to do that lmk and I can post some instructions there too.
