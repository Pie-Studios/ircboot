#IrcBoot B3 Plugin

A B3 plugin that enables remote administration via IRC 

Installation
------------
1. Install as regular B3 plugin
2. Place pyircbot.py(required dependancy) in your b3 installation folder(where b3_run.py or b3_run.exe exists)
3. Configure plugin_ircboot.xml. Instructions are in the file.


B3 Commands
-----------

	!ircadd <ingame user> - Adds user with their ingame level
	!ircadd <nick!ident@hostname mask> <level> - Adds custom mask with specific level to authlist
	!ircrem <nick!ident@hostname mask> - Removes the mask from the authlist
	!ircexec <target> <message> - Send a message from the bot to an IRC user or IRC channel.
	!ircon <rcon string> - Executes rcon command, sends any output back as pm
	
Prepend @ in IRC to broadcast to all b3 bots.

Permissions
-----------
Permissions are handled by a plain-text file specified in the xml config(downloading permissions via HTTP will become available soon).
The text file specifies which B3 level users on IRC have when they communicate with the bot(s).

The file format is:
	
	nick!ident@hostname:*b3 level*
	
NOTES: 
* B3 level is an int(1,2,10,20,40,60,80,100)
* One user per line
* The first part(before the : ) supports wildcards via *.

Example:
	
	ArmedGuy!*@*:100
	Becca!*@*.internal.network:80
	*!*@*.specific.hostname.that.gives.admin.power:60
	
	
