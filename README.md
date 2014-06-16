## Linux After install

- **Progress bar**

```bash
    $ echo 'Dpkg:Progress-Fancy "1";' | sudo tee /etc/apt/apt.conf.d/99progressbar
```

- **Extras**

```bash
    $ sudo ln -sf /lib/x86_64-linux-gnu/libudev.so.1 /lib/x86_64-linux-gnu/libudev.so.0

    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y autoconf automake  build-essential libxslt1-dev re2c libxml2 libxml2-dev bison libbz2-dev libreadline-dev libfreetype6 libfreetype6-dev libpng12-0 libpng12-dev libjpeg-dev libjpeg8-dev libjpeg8  libgd-dev libgd3 libxpm4 libssl-dev openssl gettext libgettextpo-dev libgettextpo0 libicu-dev libmhash-dev libmhash2 libmcrypt-dev libmcrypt4 python-software-properties software-properties-common g++ build-essential libssl-dev

    # Essential tools for compiling from sources
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y checkinstall cdbs devscripts dh-make fakeroot libxml-parser-perl check

    $ USERME=`whoami` && sudo ln -s /media/$USERME/Tera/Apps/SublimeText3/sublime_text /usr/bin/sublime
```

- **Puppet**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y puppet puppet-common
```

- **Curl**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y curl
```

- **php5**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y php5 php5-dev php-pear php5-cli
```

- **Mysql**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y mysql-server mysql-client libmysqlclient-dev libmysqld-dev
```

- **Postgresql**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y postgresql postgresql-client postgresql-contrib
```

- **Git**

```bash
    $ sudo add-apt-repository ppa:git-core/ppa -y && sudo apt-get update &&  sudo apt-get -o Dpkg::Progress-Fancy=true install git -y
```

- **Git Extras**

```bash
    # https://github.com/visionmedia/git-extras
    (cd /tmp && git clone --depth 1 https://github.com/visionmedia/git-extras.git && cd git-extras && sudo make install)
```

- **zsh - vim**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y \
            vim \
            zsh

    $ w=`which zsh` &&  h=`whoami` && sudo chsh -s $w $h
```

- **zssh**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y zssh
```

- **Nodejs**

``` bash
    $ sudo add-apt-repository ppa:chris-lea/node.js -y  && sudo apt-get update && sudo apt-get install -o Dpkg::Progress-Fancy=true -y  nodejs

    $ npm config set prefix ~/.npm

    $ sudo mkdir ~/tmp
    $ sudo chown -R $USER:$USER ~/tmp/
    $ sudo chown -R $USER:$USER ~/.npm

    $ cd /usr/local/share/zsh && sudo chmod -R 755 ./site-functions && sudo chown -R root:root ./site-functions && cd

cat <<-EOF >> ~/.zshrc

# |::::::::::::::::::>>>npm
# | Path for nodejs and npm
export PATH=$HOME/npm/.bin:$PATH
export NODE_PATH=/usr/lib/nodejs:/usr/lib/node:/usr/lib/node_modules:/usr/share/javascript:/usr/local/lib/node_modules:$HOME/.npm:$HOME/.npm/lib/node_modules
# |::::::::::::::::::<<<
EOF

    $ source ~/.zshrc
```

-*Packages*

```bash
    # **Bower**
    $ npm install -g bower

    # **Less**
    $ npm install -g less

    # **Yeoman**
    $ npm install -g yo

    # **Web Generator**
    $ npm install -g generator-webapp
    $ npm install -g generator-generator

```

- **NVM**

```bash
    $ curl https://raw.githubusercontent.com/creationix/nvm/v0.7.0/install.sh | sh
    $ echo "source ~/.nvm/nvm.sh" >> ~/.zshrc
    $ source ~/.nvm/nvm.sh && source ~/.nvm/nvm.sh

    # User
    # $ nvm install 0.10
    # $ nvm install 0.11
    # $ nvm use 0.10
    # $ nvm ls
```

- **Composer**

- **Autoloading**

- **Namespacing**

- **Ruby**

```bash
    $ \curl -sSL https://get.rvm.io | bash -s stable --ruby

	$ source ~/.rvm/scripts/rvm
```

- **Gufw**

```bash
    # Firewall
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y  gufw
```

- **Viewnior**

```bash
     $ URL='https://launchpad.net/~gilir/+archive/lubuntu/+files/viewnior_1.3.0-0ubuntu1%7Eppa1_amd64.deb'; FILE=`mktemp`; wget "$URL" -qO $FILE && sudo dpkg -i $FILE; rm $FILE
```

- **wkhtmltopdf**

``` bash
    # Convert html to pdf
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y  wkhtmltopdf

    Ex:
    $ wkhtmltopdf http://google.com google.pdf
```

- **pandoc**

``` bash
    # Universal document converter
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y pandoc

    # Requirements
    $ sudo apt-get install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended

    Ex:
    $ pandoc -f markdown -t html README.md >> README.html
    $ pandoc latex.md -o latex.pdf

```

- **timeshift**

``` bash
    $ sudo apt-add-repository -y ppa:teejee2008/ppa
    $ sudo apt-get update
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y timeshift
```

- **Nitro Task**

``` bash
    $ sudo add-apt-repository -y ppa:cooperjona/nitrotasks
    $ sudo apt-get update
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y nitrotasks
```

- **Install Pantheon Desktop Environment**

``` bash
    $ sudo apt-add-repository -y ppa:elementary-os/daily && sudo apt-get update && sudo apt-get install -o Dpkg::Progress-Fancy=true -y  elementary-theme elementary-icon-theme
```

- **Boot Repair**

```bash
    $ sudo add-apt-repository ppa:yannubuntu/boot-repair
    $ sudo apt-get update
    $ sudo apt-get install -y boot-repair && boot-repair
```

- **Grub Customizer**

```bash
    $ sudo add-apt-repository ppa:danielrichter2007/grub-customizer
    $ sudo apt-get update
    $ sudo apt-get install grub-customizer
```

- **Cairo-Dock**

```bash
    $ sudo add-apt-repository -y ppa:cairo-dock-team/ppa && sudo apt-get update && sudo apt-get install -o Dpkg::Progress-Fancy=true -y cairo-dock cairo-dock-plug-ins
```

- **Samba**

```bash
    $ sudo apt-get install samba system-config-samba cifs-utils winbind
```

- **Java**

```bash
    $ sudo apt-get install openjdk-7-jdk openjdk-7-jre icedtea-7-plugin
    $ sudo update-alternatives --config java
```

- **Packing software**

```bash
    $ sudo apt-get install unace rar unrar p7zip-rar p7zip zip unzip sharutils uudeview mpack arj cabextract file-roller
```

- **Steam**

```bash
    $ wget -c media.steampowered.com/client/installer/steam.deb
    $ sudo dpkg -i steam.deb
    $ sudo apt-get install -f
```

- **Filezilla**

```bash
    $ sudo apt-get install -o Dpkg::Progress-Fancy=true -y filezilla filezilla-common
```

- **Calibre**

```bash
    $ sudo apt-get install calibre
```

- **PeerGuardian Linux**

```bash
    $ sudo add-apt-repository ppa:jre-phoenix/ppa
    $ sudo apt-get update
    $ sudo apt-get install pgld pglcmd pglgui
```

- **Folder Colors**

```bash
    $ sudo add-apt-repository ppa:costales/folder-color -y && sudo apt-get update && sudo apt-get install folder-color -y && sudo apt-get install python-nemo && sudo cp /usr/share/nautilus-python/extensions/folder-color.py /usr/share/nemo-python/extensions/ && sudo sed -i 's/Nautilus/Nemo/g' /usr/share/nemo-python/extensions/folder-color.py && nemo -q
```

## Programas Necesarios

- Alsamixer
- Angry IP Scanner -  http://angryip.org/
- Bless Hex Editor
- gpick
- haroopad
- htop
- imagemagic
- luckybackup
- meld
- pac
- pidgin
- qshutdown
- shutter
- springseed
- sublime text
- timeshift
- wine



## Themes and Icons

- **iOS 7**

``` bash
    $ sudo add-apt-repository ppa:noobslab/icons
    $ sudo apt-get update
    $ sudo apt-get install ieos7-icons
```

- **Faience**

``` bash
    http://tiheum.deviantart.com/art/Faience-icon-theme-255099649

   $ sudo add-apt-repository ppa:tiheum/equinox
   $ sudo apt-get update
   $ sudo apt-get install faience-theme faience-icon-theme
```

- **Compass Icons**

``` bash
   $ sudo ppa:noobslab/nitrux-os
   $ sudo apt-get update
   $ sudo apt-get install compass-icons
```

- **Pacifica Icons**

``` bash
   $ sudo add-apt-repository ppa:fsvh/pacifica-icon-theme
   $ sudo apt-get update
   $ sudo apt-get install pacifica-icon-theme
```

- **Nitrux Icons**

``` bash
   $ sudo add-apt-repository ppa:upubuntu-com/nitrux
   $ sudo apt-get update
   $ sudo apt-get install nitruxos
```

- **Faience**

``` bash
    >>>    /usr/share/icons

    http://tiheum.deviantart.com/art/Faience-icon-theme-255099649

    $ sudo add-apt-repository ppa:tiheum/equinox
    $ sudo apt-get update && sudo apt-get install faience-theme faience-icon-theme

```

##    Comandos Basicos

- **Add Usuario**

```bash
    $ sudo adduser [newuser]
```

- **Delete User**

```bash
    $ sudo userdel [newuser]
```

- **Add User to Group**

```bash
    $ sudo adduser [user] [group]
```

- **Permisos**

```bash
    $ sudo chmod -R 755 folder/
```

- **Owner**

```bash
    $ sudo chown -R $USER:$USER vagrant/
```

- **View Folder size**

```bash
    $ du -hs .
    $ du * | sort -n

    $ du -h [FOLDER]
    $ du -hc [FOLDER]
    $ du -hs [FOLDER]
    $ du -hs .
    $ du -hs *
    du -hs . --exclude="*.txt"

        # Find 10 largest files/directories
    $ du -am /var | sort -n -r | head -n 10
    $ du -hsx * | sort -rh | head -10


```

- **Find**

```
        # Get all extensions and their respective file count in a directory
    $ find ./ -type f | grep -E ".*\.[a-zA-Z0-9]*$" | sed -e 's/.*\(\.[a-zA-Z0-9]*\)$/\1/' | sort | uniq -c | sort -n

        # Make the "tree" command pretty and useful by default
    alias tree="tree -CAFa -I 'CVS|*.*.package|.svn|.git' --dirsfirst"
```

## Otros Comandos

- **Show users - home**

```bash
    $ cat /etc/passwd |grep "/home" |cut -d: -f1
```

- **Show users all and uid**

```bash
    $ awk -F":" '{ print "User: " $1 "\t\tuid:" $3 }' /etc/passwd
```

- **Show users all**

```bash
    % cat /etc/passwd | cut -d ":" -f1
```


- **Find Dupicate files**

```bash
    find -not -empty -type f -printf "%s\n" | sort -rn | uniq -d | xargs -I{} -n1 find -type f -size {}c -print0 | xargs -0 md5sum | sort | uniq -w32 --all-repeated=separate
```

- **Find Dupicate files**

```bash
    fdupes -r .
```

- **wget**

```bash
    $ wget -r -l1 --no-parent -nH -nd -P/tmp -A".gif,.jpg,.png" http://example.com/images
```

## Ver Paquetes instalados

- **Todos los paquetes instaldados**

    $ dpkg --get-selections >> paquetes-instalados.txt


## Open ports

- **Centos**

```bash
    $ vim /etc/sysconfig/iptables

    +++
    -A INPUT -m state --state NEW -m tcp -p tcp --dport 3000 -j ACCEPT

    $ /sbin/service iptables restart
```


## SSH

    $ ssh-keygen -t rsa -b 4096

    $ ssh-keygen -t rsa -b 4096 -f  ~/.ssh/gitlab -C "www.gitlab.com"

    $ ssh-keygen -t dsa

    $ ssh-keygen -t rsa

    $ ssh -X user@host

    $ ssh-keygen -t dsa -f  /home/o/.ssh/NAME

    $ ssh-keygen -t dsa -f  /home/o/.ssh/[NAME] -C [COMENTARIO]

    $ ssh-keygen -t dsa -f  /home/o/.ssh/gitlab -C "www.gitlab.com"

- **SSH Config File**

```bash
    Host *
      ServerAliveInterval 240

    # |::::::: Virtual Machine Centos - Owncloud - Web
    Host vm26
        HostName 192.168.77.26
        Port 22
        User root
        IdentityFile ~/.ssh/turrisystem
        Compression yes
        CompressionLevel 9
        # RemoteForward 52698 127.0.0.1:52698
        # RemoteForward 52698 localhost:52698
        IdentitiesOnly yes


    ## Authentication
    # ssh -p 22 -o PubkeyAuthentication=no root@192.168.0.13

    ## Upload file
    # scp SourceFile user@host:directory/TargetFile

```

- **Upload ssh key**

```bash
    # scp ~/.ssh/id_rsa.pub user@host:~/.ssh/authorized_keys
```

- **Upload Files SSH**

```bash
    $ scp FILE USER@SERVER:LOCATION
```

## rmate

```bash
    $ curl https://raw.github.com/aurora/rmate/master/rmate > rmate

    $ sudo mv rmate /usr/local/bin
        $  sudo mv rmate ~/.local/bin

    $ sudo chmod +x /usr/local/bin/rmate

    $ sudo iptables -A INPUT -p tcp --dport 52698 -j ACCEPT


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

**Cron examples**

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

    $ sudo sublime /etc/fstab

    +++ UUID=e2a5bf75-e511-4330-9f1e-efc114b9a47e /media/oo/Tera  ext4    errors=remount-ro 0       1

```


**Descargar MountManager**

```bash
    http://ubuntuforums.org/showthread.php?t=1604251
```

**Edit fstab**
```bash
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


## Vagrant

    $ vagrant box add [name] [url]

    $ vagrant box list

    $ vagrant box remove [name]

    $ vagrant init ubuntu/trusty64

    $ vagrant init [BOX_NAME] [URL]

    $ vagrant up

    $ vagrant ssh

    $ vagrant suspend

    $ vagrant resume

    $ vagrant halt

    $ vagrant restart

    $ vagrant destroy



    config.vm.synced_folder [Local], [Vagrant box]

## PUPPET

    $ puppet apply --noop

    $ puppet apply --noop

## Web Dev Utils

- **Koala**
- **Pleeease - http://pleeease.io/**
