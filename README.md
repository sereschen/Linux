###	Programs


- Cairo-Dock
- Samba
- timeshift
- pac
- brackets
- haroopad
- meld
- qshoutdown
- shutter
- luckybackup
- Bless Hex Editor
- htop
- wine
- dbeaver
- gpick
- imagemagic
- springseed


##### dev

- nodejs
- python-software-properties
- software-properties-common
- nodejs-legacy
- npm
- yum

```bash
    # timeshift
   $ sudo apt-add-repository -y ppa:teejee2008/ppa
   $ sudo apt-get update
   $ sudo apt-get install timeshift
    
    # Nitro Task
   $ sudo add-apt-repository ppa:cooperjona/nitrotasks
   $ sudo apt-get update
   $ sudo apt-get install nitrotasks
    
    # Nodejs
   $ sudo add-apt-repository -y ppa:chris-lea/node.js
   $ sudo apt-get update
   $ sudo apt-get install nodejs
```

- - - - - - - -

### Icons


###### iOS 7
```bash
    sudo add-apt-repository ppa:noobslab/icons
    sudo apt-get update
    sudo apt-get install ieos7-icons
```

###### Faience
http://tiheum.deviantart.com/art/Faience-icon-theme-255099649
```bash
   $ sudo add-apt-repository ppa:tiheum/equinox
   $ sudo apt-get update
   $ sudo apt-get install faience-theme faience-icon-theme
```

###### Compass Icons
```bash
   $ sudo ppa:noobslab/nitrux-os
   $ sudo apt-get update
   $ sudo apt-get install compass-icons
```

###### Elementary Icons
```bash
   $ sudo ppa:noobslab/nitrux-os
   $ sudo apt-get update
   $ sudo apt-get install elementary-icon-theme
```

###### Elementary Icons
```bash
   $ sudo ppa:noobslab/nitrux-os
   $ sudo apt-get update
   $ sudo apt-get install elementary-icon-theme
```

###### Pacifica Icons
```bash
   $ sudo add-apt-repository ppa:fsvh/pacifica-icon-theme
   $ sudo apt-get update
   $ sudo apt-get install pacifica-icon-theme
```

###### Nitrux Icons
```bash
   $ sudo add-apt-repository ppa:upubuntu-com/nitrux
   $ sudo apt-get update
   $ sudo apt-get install nitruxos
```

_ _ _

### Comandos

```bash

	# Add Usuario
	sudo adduser [newuser]

	# Delete User
	sudo userdel [newuser]

	# Add User to Group
	sudo adduser [user] sudo

	# Permisos
	sudo chmod 755 [folder]/ -R

	sudo chown -R $USER:$USER vagrant/
```


- - -

### Mount Driver

```bash
	ll /dev/disk/by-uuid/ && ll /dev/disk/by-label/
    
	# /media/Tera02
	/usr/bin/udisks --mount /dev/disk/by-uuid/2fc2ea6e-a2ed-4d0f-a167-0ba68925a821


	# /media/Tera01
	/usr/bin/udisks --mount /dev/disk/by-uuid/e2a5bf75-e511-4330-9f1e-efc114b9a47e
```

### Upload Files SSH

```bash
	scp FILE USER@SERVER:LOCATION
```

### Download full website

```bash
wget \
     --recursive \
     --no-clobber \
     --page-requisites \
     --html-extension \
     --convert-links \
     --restrict-file-names=windows \
     --domains mmenu.frebsite.nl \
     --no-parent \
         mmenu.frebsite.nl/examples/responsive/
```

### Cron


- View Root User Cronjob

```bash
	$ crontab -l
```

- View Users Cronjob

```bash
	$ crontab -u userName -l
	$ crontab -u vivek -l
```

- Install or create or edit my own cron jobs

```bash
	$ crontab -e
```

- Syntax of crontab


```bash
	1 2 3 4 5 /path/to/command arg1 arg2	

	# or
	
	1 2 3 4 5 /root/backup.sh
	
	# or
	
	1 2 3 4 5 USERNAME /path/to/command arg1 arg2
	
	# Format

	* * * * * command to be executed
	- - - - -
	| | | | |
	| | | | ----- Day of week (0 - 7) (Sunday=0 or 7)
	| | | ------- Month (1 - 12)
	| | --------- Day of month (1 - 31)
	| ----------- Hour (0 - 23)
	------------- Minute (0 - 59)
```

## Prompt Especial characters
```bash
\a : an ASCII bell character (07)
\d : the date in "Weekday Month Date" format (e.g., "Tue May 26")
\D{format} : the format is passed to strftime(3) and the result is inserted into the prompt string; an empty format results in a locale-specific time representation. The braces are required
\e : an ASCII escape character (033)
\h : the hostname up to the first '.'
\H : the hostname
\j : the number of jobs currently managed by the shell
\l : the basename of the shell’s terminal device name
\n : newline
\r : carriage return
\s : the name of the shell, the basename of $0 (the portion following the final slash)
\t : the current time in 24-hour HH:MM:SS format
\T : the current time in 12-hour HH:MM:SS format
\@ : the current time in 12-hour am/pm format
\A : the current time in 24-hour HH:MM format
\u : the username of the current user
\v : the version of bash (e.g., 2.00)
\V : the release of bash, version + patch level (e.g., 2.00.0)
\w : the current working directory, with $HOME abbreviated with a tilde
\W : the basename of the current working directory, with $HOME abbreviated with a tilde
\! : the history number of this command
\# : the command number of this command
\$ : if the effective UID is 0, a #, otherwise a $
\nnn : the character corresponding to the octal number nnn
\\ : a backslash
\[ : begin a sequence of non-printing characters, which could be used to embed a terminal control sequence into the prompt
\] : end a sequence of non-printing characters
```

## Promps


- 

```
[user] [host]
[~/dir/]
$
```

``` bash
# ### Red 
PS1="\[\e[0;47m\] \[\e[m\] \[\e[0;31m\][\u] [\h] \[\e[m\] \n\[\e[0;47m\] \[\e[m\] \[\e[0;91m\][\w] \[\e[m\] \n\[\e[0;40m\] \[\e[m\] \[\e[1;30m\] $ \[\e[m\]"

PS1="${on_white} ${rs} ${red}[\u] - [\h] ${rs}
${on_white} ${rs} ${ired}[\w] ${rs}
${on_black} ${rs} ${bwhite} $ ${rs}"
```

``` bash
# ### Blue 
PS1='\[\e[0;47m\] \[\e[m\] \[\e[0;94m\][\u] [\h] \[\e[m\] \n\[\e[0;47m\] \[\e[m\] \[\e[0;34m\][\w] \[\e[m\] \n\[\e[0;40m\] \[\e[m\] \[\e[1;30m\] $ \[\e[m\]'
```

``` bash
# ### Purple 
PS1='\[\e[0;47m\] \[\e[m\] \[\e[0;35m\][\u] [\h] \[\e[m\] \n\[\e[0;47m\] \[\e[m\] \[\e[0;35m\][\w] \[\e[m\] \n\[\e[0;45m\] \[\e[m\] \[\e[1;30m\] $ \[\e[m\]'
```


----------

- 

```
user@host ~ $
```

``` bash
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;30m\][\u@\h]\[\033[01;34m\] \w \$\[\033[00m\]'
```

----------

- 

```
~/www $
```

``` bash
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;34m\] \w \$ \[\033[00m\]'
```

----------

- 

```
^_^[user@host:~/www/]$
```

``` bash
PS1="\`if [ \$? = 0 ]; then echo \[\e[33m\]^_^\[\e[0m\]; else echo \[\e[31m\]O_O\[\e[0m\]; fi\`[\u@\h:\w]\\$ "
```

----------

- 

```
Thu Jul 25 16:11:48 MDT 2013
~/www/
user@host: pts/0: 10 files 76Kb ->
```

``` bash
PS1="\n\[\033[35m\]\$(/bin/date)\n\[\033[32m\]\w\n\[\033[1;31m\]\u@\h: \[\033[1;34m\]\$(/usr/bin/tty | /bin/sed -e 's:/dev/::'): \[\033[1;36m\]\$(/bin/ls -1 | /usr/bin/wc -l | /bin/sed 's: ::g') files \[\033[1;33m\]\$(/bin/ls -lah | /bin/grep -m 1 total | /bin/sed 's/total //')b\[\033[0m\] -> \[\033[0m\]"
```
----------

- 

```
[user] - [host] - [16:50:44]
    [~/www/]
        ^_^ --> $
```

``` bash
PS1="\[\033[1;36m\] [\u] - [\h] - [\t] \[\033[0m\]  \n  \[\033[1;34m\] [\w] \[\033[1;34m\] \n     ^_^ --> $ \[\033[0m\]"
```
----------





