###	Programas Necesarios


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
- npm
- yum

```bash
    # timeshift
    sudo apt-add-repository -y ppa:teejee2008/ppa
    sudo apt-get update
    sudo apt-get install timeshift
    
    # Nitro Task
    sudo add-apt-repository ppa:cooperjona/nitrotasks
    sudo apt-get update
    sudo apt-get install nitrotasks
    
    # Nodejs
    sudo add-apt-repository -y ppa:chris-lea/node.js
    sudo apt-get update
    sudo apt-get install nodejs
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
    sudo add-apt-repository ppa:tiheum/equinox
    sudo apt-get update
    sudo apt-get install faience-theme faience-icon-theme
```

###### Compass Icons
```bash
   sudo ppa:noobslab/nitrux-os
   sudo apt-get update
   sudo apt-get install compass-icons
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



	
