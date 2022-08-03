# PS4-Hacking/Homebrew

## Idea
I have an old PS4 I have not used for about a year sitting around gathering dust while I wait to see if I buy a PS5 or a steamdeck.
I have "hacked" many consoles in the past including the Xbox, Xbox360, Wi and PS3 so I had been keeping an eye out on the status of a jailbreak for the PS4.

I was searching for datasheets on the Wemos ESP32 S2 mini and came across a port about jailbreaking the PS4 with one so I was very curious indeed.
It turns out you need a specific version number of system software on the PS4 to be able to jailbreak it, at the moment you need to be running V9.0 or below.
Lucky for me I had not updated my PS4 in a long time and it was on V9.0!

This project is more of a tutorial and links to the resources I used to jailbreak my PS4.


## Parts used

- Wemos ESP32 S2 mini
- USB to SATA cradle for the SSD
- 250gig SSD


## Coding
Here is a list of steps and also links to the sites and videos that will help jailbreak a V9.0 PS4.

You can do all of this with a memory stick but I thought it would be more interesting to use the ESP32 S2 mini with its USB emulation to do the same job a lot faster.

### Background
I did a lot of research watching these to Youtube channels.
https://www.youtube.com/c/mbcrump
Michael is a coder and understands the coding involved and was the first video I watched on the ESP32 S2 method.
https://www.youtube.com/c/MODDEDWARFARE
This guy has a lot of really well explained videos on all things to do with PS homebrew and more. 

### Uploading a new firmware to the ESP32 S2
has made a really handy site where you can use the ESP webflasher to flash direct over the USB data cable direct in the browser.
https://mbcrump.github.io/ESP32-S2-AUTO-INSTALL/
Once installed then all you need to do is connect it to the USB of the PS4.
### Activating the jailbreak
First of all go into the PS4 settings and software update and turn off automatic system software updates.
Change the network settings in the settings panel to make the PS4 connect via wifi.

A list of available wifi AP will appear and you should choose PS4 WEB which is the ESP32 S2 mini.
You can test the connection and it will find the AP and give you an IP via DHCP but it will not be connected to the internet which is a good thing at this point.
Then go into the web browser and goto this URL http://10.1.1.1
This is the IP of the the ESP32 S2 mini.

You should see a page with the option to run the Goldhen jailbreak and also a setting to control the onboard fan speed.
Run Goldhen and wait, there could be a couple of errors you have to say OK to but it if it works you should see a notification that Goldhen has been launched. Sometimes it crashes and does not jailbreak in this case reboot the PS4 and try again.

You can check if the jailbreak has worked by checking in the settings menu, right at the top should be a new Goldhen menu.
In there you can start the ftp server and bitloader.

Once jailbroken I tend to then go back to the settings and change over to a LAN cable for internet use.
To do this "safely" you want to change the DNS settings so that the sony servers can be blocked.

I use these DNS servers

192.241.221.79

165.227.83.145

### Homebrew Store

By installing the [HomebrewStore](https://github.com/LightningMods/PS4-Store) you really open up what the jailbreak can do!
There are so many useful tools in there to help you dump your own disc games, a file manager, internal pkg installer, game file updates, save game tools and much more.
### Handy Tools
https://darthsternie.net/ps4-firmwares/
Is a good place to get the system software recovery images for the correct version of the software.
I have used this to rebuild a new hard drive in the PS4 and keep it at V9.0

https://defaultdnb.github.io a place to search for your disc games and see what level of game patch will work on your firmware.

https://github.com/hippie68/ftpdump to dump the contents of a game disc to a network drive via FTP.

http://karo218.ir a page that you can load up in the PS4 browser and it allows you to jailbreak with Goldhen and also other payloads such as a different ftp server than the Goldhen one and also an update blocker payload.

https://nightkinghost.com same as above.


## Construction
Not really much to here apart from plugging in the ESP32 S2 and executing the payloads.


## Conclusion
It took a long time to find out the software and methods used because there was a lot of out of date information out there and just plain wrong information but it was worth it in the end.

I now have digital copies of all my disc games sitting on my NAS and can FTP them to the PS4 for install at any time.
All the games are patched to the highest level so all bug fixes and in some cases extra content I did not have before on the retail disc install.

The next step is to install some Linux based console emulators so that I can turn the PS4 into a retro games machine with hundreds of games from different consoles like the N64, Sega Saturn, SNES.

Cost of this project was minimal, the ESP32 S2 mini cost about 8 euro and I had a good data cable lying around spare.
Same thing with the SSD I use to dump my games to, I was searching for a USB of something that I could use and found this old "broken" SSD and it now works perfectly.

By doing all of this I have brought this old PS4 back to life, so now I will go hunting on second sites for cheap disc games and then dump them to my NAS drive.

A really cheap and simple project in the end and hopefully many hours of gaming to come.


