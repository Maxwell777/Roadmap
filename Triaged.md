Triaged reports

Not a bug
---------
	- settings/backgrounds Consider aligning the dropdown boxes for Gradient and Picture Aspect to each other.
	- If changing the mouse pointer from default white to black (e.g Adwaita), it shows up as white during startup. After login, it changes to black.
	- uim and uim-byeoru combination give us a good process but , uim installs only uim itself , we need key instance to define keys to input language. installing other packages supported by uim category , it install 19 more packages we just need one more package “uim-byeoru” with “uim”
	- the Xfce terminal’s menu bar doesn’t show (by design, ALT is used by some command-line tools such as nano, menu is accessible via right-click)
	- the title “Menu” isn’t shown next to the Mint icon for the menu, as in the other desktop environments.

Outside of the scope
--------------------


Can't reproduce
---------------
	- mdm: The login screen always defaults to “Login” rather than the user. In my case I have one user on the system and it should default to that user so I don’t have to continually click on my user to input the password.
	- The wireless signal strength of the networks shown changes constantly and the percentage is almost all the time wrong (weak signal networks are shown with 80+% strength and strong signal ones with low percentage).
	- caja exits (“normally”) on clicking “smb-network”.
	- mate: Audio-preview causes the window in question to freeze, requiring the user to forcibly close it. Just moving the mouse pointer over the audio file is enough to cause it to lock up at times. Happens 25-50% of the time.
	- mate: Movie Player closes without an error message when switching from full-screen. This happens with both audio & video files and whether you double-click on Movie Player or select ‘Leave Fullscreen’. Happens about 50% of the time.
	- kde: When running the live system it sees and connects to my wireless network (WPA2/PSK) with no problems and installation proceeds normally. On reboot, it fails to connect to the same SSID — just keeps attempting to connect and asking again for the password. I reinstalled and the bug was reproducable. It does not appear to affect Mint 17 KDE however; just 17.1RC. I wonder if it might be related to the new KWallet integration.
	- whiskermenu: Le placement du raccourci dans la barre de tache est aussi aléatoire, il est dommage qu’il ne se mette pas directement à côté des autres raccourcis rapides.
	- xfce: language indicator in system tray area is missing (it needs to be added to the panel indeed, but that's because it won't hide itself if there's only one layout defined)
	- xfce: Window edges don’t seem as grabby as on Cinnamon 17.1 Is this tweakable via a GTK config file?
	- xfce64bit: Clicking the “Install Linux Mint” icon on the desktop produced a lengthy popup error message about trouble mounting /dev/sdc1 (the USB stick holding the image). Same error after manually mounting or unmounting the stick. The install option in the menu worked normally

Upstream
--------
	- ubiquity: Selecting Encrypted Home Folder Always Breaks Swap https://bugs.launchpad.net/linuxmint/+bug/1367392
	- caribou: the tray button does not send the keyboard to the tray, otherwise the applet works fine.
	- pidgin: status icon is not showing even if in the settings it’s set to always show.
	- Add some template such as Writer, Calc, Presentation on context R_click (need ability to define system-wide templates for nemo/caja, but we also need them to be translatable..)
	- Could you add nabi as input method to mintlocale? (it needs to be supported by im-config first)
	- gcin couldn’t apply the change of its input method settings, and also the CTRL+SPACE(combine keys that used change bwtween English and Chinese input method) didn’t work well seems these could be fixed by simply update the gcin to ver 2.8.2 --> Please create an issue on github.com/linuxmint/mintlocale. We need directions to reproduce this.
	- mate:
		- alt-mouse wheel desktop zoom
		- Flash video in website doesn't inhibit monitor turning itself off	(https://github.com/mate-desktop/mate-screensaver/issues/57)
		- brightness OSD doesn't work (with Marco) https://github.com/mate-desktop/mate-power-manager/issues/110
		- Movie Player’s screensaver/display-sleep-inhibit feature (still) doesn’t work. When enabled, either the screensaver and/or Powermanager’s display-sleep feature cuts in on queue.
		- mcc->notifications->help button doesn't work
	- Compiz GTK decorator segfaults in Virtualbox
	- kde:
		- problem with CalDAV/CardDAV-Servers… If I create an event in KOrganizer, it only works once and then is broken (no syncing) until I delete the calendar and add it again. Works fine in 17, using tine 2.0 WebDAV-Server - https://forum.kde.org/viewtopic.php?f=261&t=124072
	- whiskermenu:
		- lorsque je veux mettre un programme depuis le menu sur le bureau j’ai droit au popup qui veux que je mette ce raccourci en tant qu’exécutable… Dommage pour les néophyte… --> https://github.com/gottcode/xfce4-whiskermenu-plugin/pull/100
		- Only the items on the right-hand side of the menu can be selected with my keyboard. https://github.com/gottcode/xfce4-whiskermenu-plugin/issues/101
	- QT5: Dropbox icon is not displayed in the panel, but Dropbox daemon loads and functions as usual. I’ve seen this elsewhere, and seen numerous similar complains. I suspect it’s related to the new QT-based Dropbox release. https://www.dropboxforum.com/hc/communities/public/questions/201545695-After-upgrade-to-3-x-the-dropbox-tray-icon-is-missing-XFCE-Xubuntu-14-04-1-x64-?locale=en-us
