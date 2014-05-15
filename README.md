## Linux After install

1.

```bash
	$ cd /lib/x86_64-linux-gnu/
  $ sudo ln -s libudev.so.1 libudev.so.0
```


## Programas Necesarios


- Alsamixer
- Angry IP Scanner -  http://angryip.org/
- Bless Hex Editor
- brackets
- Cairo-Dock
- dbeaver
- gpick
- haroopad
- htop
- imagemagic
- luckybackup
- meld
- pac
- pidgin
- qshutdown
- Samba
- shutter
- springseed
- sublime text
- timeshift
- wine

- ** wkhtmltopdf **

``` bash 
    # Convert html to pdf 
    $ sudo apt-get install wkhtmltopdf -y

    Ex:
    $ wkhtmltopdf http://google.com google.pdf
```

- ** pandoc **

``` bash
    # Universal document converter
    $ sudo apt-get install pandoc -y

    # Requerments
    $ sudo apt-get install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended



    Ex:
    $ pandoc -f markdown -t html README.md >> README.html
    $ pandoc latex.md -o latex.pdf

```
 

** dev **

- python-software-properties
- software-properties-common
- yum

** npm **

```bash
    $ sudo apt-get -y install npm
```

** Less **

```bash
    $ sudo npm install less -g
    $ sudo ln -s /usr/bin/nodejs /usr/bin/node
```

** timeshift **

``` bash
    $ sudo apt-add-repository -y ppa:teejee2008/ppa
    $ sudo apt-get update
    $ sudo apt-get install timeshift
```

** Nitro Task **

``` bash
    $ sudo add-apt-repository ppa:cooperjona/nitrotasks
    $ sudo apt-get update
    $ sudo apt-get install nitrotasks
```

** Nodejs **

``` bash
    $ sudo add-apt-repository -y ppa:chris-lea/node.js
    $ sudo apt-get update
    $ sudo apt-get install nodejs
```

** Install Pantheon Desktop Environment **

``` bash
    $ sudo apt-add-repository ppa:elementary-os/daily
    $ sudo apt-add-repository ppa:marlin-devs/marlin-daily
    $ sudo apt-add-repository ppa:ricotz/docky
    $ sudo apt-get update
    $ sudo apt-get install pantheon-shell pantheon midori lingot wingpanel plank pantheon-terminal pantheon-xsession-settings contractor slingshot-launcher scratch marlin elementary-theme elementary-icon-theme ttf-droid footnote switchboard plank-theme-pantheon snap preload
```

## Themes and Icons

** iOS 7 **

``` bash
    $ sudo add-apt-repository ppa:noobslab/icons
    $ sudo apt-get update
    $ sudo apt-get install ieos7-icons
```

** Faience **

``` bash
    http://tiheum.deviantart.com/art/Faience-icon-theme-255099649

   $ sudo add-apt-repository ppa:tiheum/equinox
   $ sudo apt-get update
   $ sudo apt-get install faience-theme faience-icon-theme
```

** Compass Icons **

``` bash
   $ sudo ppa:noobslab/nitrux-os
   $ sudo apt-get update
   $ sudo apt-get install compass-icons
```

** Pacifica Icons **

``` bash
   $ sudo add-apt-repository ppa:fsvh/pacifica-icon-theme
   $ sudo apt-get update
   $ sudo apt-get install pacifica-icon-theme
```

** Nitrux Icons **

``` bash
   $ sudo add-apt-repository ppa:upubuntu-com/nitrux
   $ sudo apt-get update
   $ sudo apt-get install nitruxos
```

** Faience **

``` bash
    >>>    /usr/share/icons

    http://tiheum.deviantart.com/art/Faience-icon-theme-255099649

    $ sudo add-apt-repository ppa:tiheum/equinox
    $ sudo apt-get update && sudo apt-get install faience-theme faience-icon-theme

```

##    Comandos Basicos

** Add Usuario **

```bash
    $ sudo adduser [newuser]
```

** Delete User **

```bash
    $ sudo userdel [newuser]
```

** Add User to Group **

```bash
    $ sudo adduser [user] [group]
```

** Permisos **

```bash
    $ sudo chmod -R 755 folder/
```

** Owner **
```bash
    $ sudo chown -R $USER:$USER vagrant/
```

## Otros Comandos

** Show users - home **

```bash
    $ cat /etc/passwd |grep "/home" |cut -d: -f1
```

** Show users all and uid **

```bash
    $ awk -F":" '{ print "User: " $1 "\t\tuid:" $3 }' /etc/passwd
```

** Show users all **

```bash
    % cat /etc/passwd | cut -d ":" -f1
```


** Find Dupicate files **

```bash
    find -not -empty -type f -printf "%s\n" | sort -rn | uniq -d | xargs -I{} -n1 find -type f -size {}c -print0 | xargs -0 md5sum | sort | uniq -w32 --all-repeated=separate
```

** Find Dupicate files **

```bash
    fdupes -r .
```

** wget **

```bash
    $ wget -r -l1 --no-parent -nH -nd -P/tmp -A".gif,.jpg,.png" http://example.com/images
```

## Ver Paquetes instalados

** Todos los paquetes instaldados **

    $ dpkg --get-selections >> paquetes-instalados.txt


## Open ports

** Centos **

```bash
    $ vim /etc/sysconfig/iptables

    +++
    -A INPUT -m state --state NEW -m tcp -p tcp --dport 3000 -j ACCEPT

    $ /sbin/service iptables restart
```


## SSH

    $ ssh-keygen -t rsa -b 4096

    $ ssh-keygen -t dsa

    $ ssh-keygen -t rsa

    $ ssh -X user@host

    $ ssh-keygen -t dsa -f  /home/o/.ssh/NAME

    $ ssh-keygen -t dsa -f  /home/o/.ssh/[NAME] -C [COMENTARIO]

    $ ssh-keygen -t dsa -f  /home/o/.ssh/gitlab -C "www.gitlab.com"

## Upload Files SSH

```bash
    $ scp FILE USER@SERVER:LOCATION
```

## Download full website

```bash
    $ wget \
        -p \
        --recursive \
        --no-clobber \
        --page-requisites \
        --html-extension \
        --convert-links \
        --restrict-file-names=windows \
        --domains www.atlassian.com \
        --no-parent \
            www.atlassian.com/es/git/workflows
```

## Cron

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

** Cron examples **

```bash
    # Pull and log
    */1 * * * *   /root/crons/prototiposena.sh  >> /root/crons/logs/prototiposena.$(date +\%Y\%m\%d).log 2>&1
    */1 * * * *   /root/crons/time_stamp.sh  >> /root/crons/logs/prototiposena.$(date +\%Y\%m\%d).log 2>&1


    */3 * * * *   /root/crons/prototiposena_prueba.sh  >> /root/crons/logs/prototiposena_prueba.$(date +\%Y\%m\%d).log 2>&1
    */3 * * * *   /root/crons/time_stamp.sh  >> /root/crons/logs/prototiposena_prueba.$(date +\%Y\%m\%d).log 2>&1


    # prototiposena_dropbox.sh
    00 20 * * *    /root/crons/prototiposena_dropbox.sh  >> /root/crons/logs/prototiposena_dropbox.$(date +\%Y\%m\%d).log 2>&1
    00 20 * * *    /root/crons/time_stamp.sh  >> /root/crons/logs/prototiposena_dropbox.$(date +\%Y\%m\%d).log 2>&1

    # Remove file older than 7 days
    0 0 * * *     find /root/crons/logs -mtime +7 -exec rm {} \;
```


## Keymap cambiar techas

#### Usando el comando `xmodmap`

-  Crear archivo

```bash
    $ touch ~/.xmodmap
    $ vim ~/.xmodmap
```

- Editar .xmodmap agregando:

```bash
    !
    ! make shift-, be < and shift-. be >
    !
    keysym comma = comma semicolon less less less
    keysym period = period colon greater greater greater


    !
    ! Add <> to zx
    ! ORIGINAL
    ! keycode  52 = z Z z Z guillemotleft less guillemotleft less
    ! keycode  53 = x X x X guillemotright greater guillemotright greater
    !
    keycode  52 = z Z z Z guillemotleft less less less
    keycode  53 = x X x X guillemotright greater greater greater

```

- Ejecutar

```bash
    xmodmap -verbose ~/.xmodmap
```

## Otros comados utiles

- Ver teclas

```bash
    $ xmodmap -pke | less
```

- Ver las lista de dispositivos

```bash
    $ xinput list
```

- Diagnostico de las teclas

```bash
    $ xinput query-state 9
```

## Config Bandwidth

```bash
    $ sudo apt-get install trickle
```



## Montar Driver

```bash
    $ ll /dev/disk/by-uuid/ && ll /dev/disk/by-label/

    /media/Tera02
    /usr/bin/udisks --mount /dev/disk/by-uuid/2fc2ea6e-a2ed-4d0f-a167-0ba68925a821


    /media/Tera01
    /usr/bin/udisks --mount /dev/disk/by-uuid/e2a5bf75-e511-4330-9f1e-efc114b9a47e
```


** Descargar MountManager **

```bash
    http://ubuntuforums.org/showthread.php?t=1604251
```

** Edit fstab **
```bash
    $ sudo sublime /etc/fstab

    $ sudo blkid -c /dev/null

    +++ UUID=3ABC75AEBC756573 /home/o/Media/Disk-2  ntfs-3g defaults,auto,uid=1000,gid=1000,umask=002 0 0

    or /* BEST OPTION install NTFS config */

    +++ UUID=55aa3897-145f-4dc3-8d23-1e27c804e7ba    /    ext4    errors=remount-ro    0    1
        /dev/sda3    /home/o/Media/Disk-2    ntfs-3g    defaults,rw,users,auto,uid=0000,gid=1000,fmask=000,dmask=000,umask=000    0    0

    or

     UUID=3ABC75AEBC756573 /home/o/Media/Disk-2  ntfs-3g defaults,rw,users,auto,uid=0000,gid=1000,fmask=000,dmask=000,umask=000 0 0000
```

## Descomprimir a traves de php

```php
    <?php
        exec('tar -xzf SecretariaSalud.tar.gz',$ret);
    ?>
```
