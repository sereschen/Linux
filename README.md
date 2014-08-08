# Linux After install

- **Progress bar**

```sh
    $ echo 'Dpkg:Progress-Fancy "1";' | sudo tee /etc/apt/apt.conf.d/99progressbar
```

- **Extras**

```sh
    $ sudo ln -sf /lib/x86_64-linux-gnu/libudev.so.1 /lib/x86_64-linux-gnu/libudev.so.0

    $ sudo apt install -y autoconf automake  build-essential libxslt1-dev re2c libxml2 libxml2-dev bison libbz2-dev libreadline-dev libfreetype6 libfreetype6-dev libpng12-0 libpng12-dev libjpeg-dev libjpeg8-dev libjpeg8  libgd-dev libgd3 libxpm4 libssl-dev openssl gettext libgettextpo-dev libgettextpo0 libicu-dev libmhash-dev libmhash2 libmcrypt-dev libmcrypt4 python-software-properties software-properties-common g++ build-essential libssl-dev pkg-config

    # Essential tools for compiling from sources
    $ sudo apt install -y checkinstall cdbs devscripts dh-make fakeroot libxml-parser-perl check

    $ USERME=`whoami` && sudo ln -s /media/$USERME/Tera/Apps/SublimeText3/sublime_text /usr/bin/sublime
```

- **Puppet**

```sh
    $ sudo apt install -y puppet puppet-common
```

- **Curl**

```sh
    $ sudo apt install -y curl
```

- **php5**

```sh
    $ sudo apt install -y php5 php5-dev php-pear php5-cli
```

- **Mysql**

```sh
    $ sudo apt install -y mysql-server mysql-client libmysqlclient-dev libmysqld-dev
```

- **Postgresql**

```sh
    $ sudo apt install -y postgresql postgresql-client postgresql-contrib
```

- **Git**

```sh
    $ sudo add-apt-repository ppa:git-core/ppa -y && sudo apt update &&  sudo apt install git -y
```

- **Git Extras**

```sh
    # https://github.com/visionmedia/git-extras
    (cd /tmp && git clone --depth 1 https://github.com/visionmedia/git-extras.git && cd git-extras && sudo make install)
```

- **zsh - vim**

```sh
    $ sudo apt install -y \
            vim \
            zsh

    $ w=`which zsh` &&  h=`whoami` && sudo chsh -s $w $h
```

## Installing ZSH

```bash
    $ sudo apt-get update

    $ sudo apt-get install -y \
        curl \
        vim \
        git \
        zsh
```

- **Installing Oh-My-ZSH**

```bash
    $ curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | bash
```

- **Setting ZSH as the default shell (instead of bash)**

```bash
    $ w=`which zsh` &&  h=`whoami` && sudo chsh -s $w $h
```

- **Install antigen**

```bash
    $ cd ~ && git clone https://github.com/zsh-users/antigen.git .antigen
```

- **Install antigen - Add**
    >>> ~/.zshrc

```bash
cat <<-EOF >> ~/.zshrc
# |::::::::::::::::::>>>zsh
source "$HOME/.antigen/antigen.zsh"

# antigen bundle command-not-found
# antigen bundle fabric
# antigen bundle heroku
# antigen bundle kennethreitz/autoenv
# antigen bundle lein
# antigen bundle pip
# antigen bundle rake
# antigen bundle rvm
# antigen bundle sprunge
# antigen bundle vundle

antigen bundle bundler
antigen bundle node
antigen bundle python
antigen bundle npm
antigen bundle history
antigen bundle rsync
antigen-bundle vagrant
antigen bundle git
antigen bundle zsh-users/zsh-completions src
antigen-bundle arialdomartini/oh-my-git
antigen-bundle zsh-users/zsh-history-substring-search
antigen-bundle zsh-users/zsh-syntax-highlighting

antigen theme Mayccoll/oh-my-git-themes arrow-green

antigen-apply
# |::::::::::::::::::<<<zsh
EOF
```

- **Fix Errors**
$ rm ~/.antigen/repos/https-COLON--SLASH--SLASH-gi* -rf

- **zssh**

```sh
$ sudo apt install -y zssh
```

### Installing ZSH Centos

```bash
    $ yum install zsh

    $ h=`whoami` && usermod -s /bin/zsh $h
```


- **Nodejs**

``` bash

    # :::::::: Method1
    $ apt-get install python g++ wget libssl-dev
    $ mkdir /tmp/nodejs && cd /tmp/nodejs
    $ wget http://nodejs.org/dist/node-latest.tar.gz
    $ tar xzvf node-latest.tar.gz && cd node-v*
    $ ./configure
    $ make
    $ make test
    $ make install
    # :::::::: .Method1

    # :::::::: Method2
    $ sudo add-apt-repository ppa:chris-lea/node.js -y  && sudo apt update && sudo apt install -y  nodejs
    $ npm config set prefix ~/.npm
    $ sudo mkdir ~/tmp
    $ sudo mkdir ~/npm
    $ sudo chown -R $USER:$USER ~/tmp/
    $ sudo chown -R $USER:$USER ~/.npm
    $ sudo npm update -g
    $ sudo chown -R $USER:$USER ~/.npm
    # ::::::: .Method2


cat <<-EOF >> ~/.zshrc
# |::::::::::::::::::>>>npm
# | Path for nodejs and npm
export PATH=$HOME/npm/.bin:$PATH
export NODE_PATH=/usr/lib/nodejs:/usr/lib/node:/usr/lib/node_modules:/usr/share/javascript:/usr/local/lib/node_modules:$HOME/.npm:$HOME/.npm/lib/node_modules
export PATH=$HOME/.npm/bin:$PATH
# |::::::::::::::::::<<<npm
EOF

    $ source ~/.zshrc
```

-*Packages*

```sh
    $ npm install -g bower
    $ npm install -g less
    $ npm install -g grunt
    $ npm install -g grunt-cli


    # **Watch files and run a command when they change**
    $ npm install -g wr

    # **Yeoman**
    $ npm install -g yo

    # **Web Generator**
    $ npm install -g generator-webapp
    $ npm install -g generator-generator

```

- **NVM**

```sh
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

- **Phython**

```sh
  $ sudo apt-get install python-dev libxml2-dev libxslt1-dev antiword poppler-utils pstotext

  $ wget https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py

  $ sudo python ez_setup.py

  $ sudo easy_install pip

  $ sudo pip install textract
```

```sh
    $ \curl -sSL https://get.rvm.io | bash -s stable --ruby

    $ source ~/.rvm/scripts/rvm
```

- **Gufw**

```sh
    # Firewall
    $ sudo apt install -y  gufw
```

- **Viewnior**

```sh
     $ URL='https://launchpad.net/~gilir/+archive/lubuntu/+files/viewnior_1.3.0-0ubuntu1%7Eppa1_amd64.deb'; FILE=`mktemp`; wget "$URL" -qO $FILE && sudo dpkg -i $FILE; rm $FILE
```

- **wkhtmltopdf**

``` bash
    # Convert html to pdf
    $ sudo apt install -y  wkhtmltopdf

    Ex:
    $ wkhtmltopdf http://google.com google.pdf
```

- **pandoc**

``` bash
    # Universal document converter
    $ sudo apt install -y pandoc

    # Requirements
    $ sudo apt install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended

    Ex:
    $ pandoc -f markdown -t html README.md >> README.html
    $ pandoc latex.md -o latex.pdf

```

- **timeshift**

``` bash
    $ sudo apt-add-repository -y ppa:teejee2008/ppa
    $ sudo apt update
    $ sudo apt install -y timeshift
```

- **Nitro Task**

``` bash
    $ sudo add-apt-repository -y ppa:cooperjona/nitrotasks
    $ sudo apt update
    $ sudo apt install -y nitrotasks
```

```sh
    $ sudo apt install -y daemonfs
```

- **Install Pantheon Desktop Environment**

```sh
    $ sudo apt-add-repository -y ppa:elementary-os/daily && sudo apt update && sudo apt install -y  elementary-theme elementary-icon-theme
```

- **Boot Repair**

```sh
    $ sudo add-apt-repository ppa:yannubuntu/boot-repair
    $ sudo apt update
    $ sudo apt install -y boot-repair && boot-repair
```

- **Grub Customizer**

```sh
    $ sudo add-apt-repository -y ppa:danielrichter2007/grub-customizer; sudo apt update; sudo apt install -y grub-customizer
```

- **Cairo-Dock**

```sh
    $ sudo add-apt-repository -y ppa:cairo-dock-team/ppa && sudo apt update && sudo apt install -y cairo-dock cairo-dock-plug-ins
```

- **Samba**

```sh
    $ sudo apt install samba system-config-samba cifs-utils winbind
```

- **Sigil**

```sh
    $ sudo add-apt-repository -y ppa:sunab/sigil-git; sudo apt -y update; sudo apt install sigil
```

- **Java**

```sh
    $ sudo apt install openjdk-7-jdk openjdk-7-jre icedtea-7-plugin
    $ sudo update-alternatives --config java
```

- **Packing software**

```sh
    $ sudo apt install unace rar unrar p7zip-rar p7zip zip unzip sharutils uudeview mpack arj cabextract file-roller
```

- **Steam**

```sh
    $ wget -c media.steampowered.com/client/installer/steam.deb
    $ sudo dpkg -i steam.deb
    $ sudo apt install -f
```

- **Filezilla**

```sh
    $ sudo apt install -y filezilla filezilla-common
```

- **Calibre**

```sh
    $ sudo apt install calibre
```

- **PeerGuardian Linux**

```sh
    $ sudo add-apt-repository ppa:jre-phoenix/ppa
    $ sudo apt update
    $ sudo apt install pgld pglcmd pglgui
```

- **Folder Colors**

```sh
    $ sudo add-apt-repository ppa:costales/folder-color -y && sudo apt update && sudo apt install folder-color -y && sudo apt install python-nemo && sudo cp /usr/share/nautilus-python/extensions/folder-color.py /usr/share/nemo-python/extensions/ && sudo sed -i 's/Nautilus/Nemo/g' /usr/share/nemo-python/extensions/folder-color.py && nemo -q
```

- **XBMC**

```sh
    $ sudo add-apt-repository ppa:team-xbmc/ppa; sudo apt update; sudo apt install -y xbmc
```

## **VNC**

- Update

```sh
    $ apt update; apt dist-upgrade -y --force-yes
```

```sh
    $ apt install xubuntu-desktop xfce4 firefox nano -y --force-yes
```

- Install VNC

```sh
    $ apt install vnc4server
```

- check

```sh
    $ dpkg -l | grep vnc
```

- Add user

```sh
    $ adduser master
```

- Config VNC

```sh
    $ su - master
    $ vncserver
    $ cp ~/.vnc/xstartup ~/.vnc/xstartup.bak
    $ > ~/.vnc/xstartup
    $ vi ~/.vnc/xstartup
```

```sh
#!/bin/sh
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
startxfce4 &

[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
```


```sh
    $ vncserver -kill :1
    $ exit
    $ vi /etc/init.d/vncserver
```

```shell
    #!/bin/bash

    unset VNCSERVERARGS
    VNCSERVERS=""
    [ -f /etc/vncserver/vncservers.conf ] && . /etc/vncserver/vncservers.conf
    prog=$"VNC server"
    start() {
        . /lib/lsb/init-functions
        REQ_USER=$2
        echo -n $"Starting $prog: "
        ulimit -S -c 0 >/dev/null 2>&1
        RETVAL=0
        for display in ${VNCSERVERS}
        do
        export USER="${display##*:}"
        if test -z "${REQ_USER}" -o "${REQ_USER}" == ${USER} ; then
        echo -n "${display} "
        unset BASH_ENV ENV
        DISP="${display%%:*}"
        export VNCUSERARGS="${VNCSERVERARGS[${DISP}]}"
        su ${USER} -c "cd ~${USER} && [ -f .vnc/passwd ] && vncserver :${DISP} ${VNCUSERARGS}"
        fi
        done
    }
    stop() {
        . /lib/lsb/init-functions
        REQ_USER=$2
        echo -n $"Shutting down VNCServer: "
        for display in ${VNCSERVERS}
        do
        export USER="${display##*:}"
        if test -z "${REQ_USER}" -o "${REQ_USER}" == ${USER} ; then
        echo -n "${display} "
        unset BASH_ENV ENV
        export USER="${display##*:}"
        su ${USER} -c "vncserver -kill :${display%%:*}" >/dev/null 2>&1
        fi
        done
        echo -e "\n"
        echo "VNCServer Stopped"
    }
    case "$1" in

        start)
            start $@
        ;;

        stop)
            stop $@
        ;;

        restart|reload)
            stop $@
            sleep 3
            start $@
        ;;

        condrestart)
            if [ -f /var/lock/subsys/vncserver ]; then
                stop $@
                sleep 3
                start $@
            fi
        ;;

        status)
            status Xvnc
        ;;

        *)
        echo $"Usage: $0 {start|stop|restart|condrestart|status}"
        exit 1
    esac

```

```sh
    $ chmod +x /etc/init.d/vncserver
    $ mkdir -p /etc/vncserver
    $ vi /etc/vncserver/vncservers.conf
```

```sh
    VNCSERVERS="1:master 2:root"

    VNCSERVERARGS[1]="-geometry 1440x768"
    VNCSERVERARGS[1]="-geometry 1920x1080 -depth 24"
    VNCSERVERARGS[1]="-geometry 800x600 -depth 8"

    VNCSERVERARGS[2]="-geometry 1440x768"
    VNCSERVERARGS[2]="-geometry 1920x1080 -depth 24"
    VNCSERVERARGS[2]="-geometry 800x600 -depth 8"
```

```sh
    $ update-rc.d vncserver defaults 99
    $ reboot
```
- Start VNC

```sh
    $ vnc4server
```

## **Programas Necesarios**

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
    $ sudo apt update
    $ sudo apt install ieos7-icons
```

- **Faience**

``` bash
    http://tiheum.deviantart.com/art/Faience-icon-theme-255099649

   $ sudo add-apt-repository ppa:tiheum/equinox
   $ sudo apt update
   $ sudo apt install faience-theme faience-icon-theme
```

- **Compass Icons**

``` bash
   $ sudo ppa:noobslab/nitrux-os
   $ sudo apt update
   $ sudo apt install compass-icons
```

- **Pacifica Icons**

``` bash
   $ sudo add-apt-repository ppa:fsvh/pacifica-icon-theme
   $ sudo apt update
   $ sudo apt install pacifica-icon-theme
```

- **Nitrux Icons**

``` bash
   $ sudo add-apt-repository ppa:upubuntu-com/nitrux
   $ sudo apt update
   $ sudo apt install nitruxos
```

- **Faience**

``` bash
    >>>    /usr/share/icons

    http://tiheum.deviantart.com/art/Faience-icon-theme-255099649

    $ sudo add-apt-repository ppa:tiheum/equinox
    $ sudo apt update && sudo apt install faience-theme faience-icon-theme

```

##    Comandos

- **Add Usuario**

```sh
    $ sudo adduser [newuser]
```

- **Delete User**

```sh
    $ sudo userdel [newuser]
```

- **Add User to Group**

```sh
    $ sudo adduser [user] [group]
```

- **Permisos**

```sh
    $ sudo chmod -R 755 folder/
```

- **Owner**

```sh
    $ sudo chown -R $USER:$USER vagrant/
```

- **View Folder size**

```sh
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

### **Find**

-  **Get all extensions and their respective file count in a directory**

```sh
    $ find ./ -type f | grep -E ".*\.[a-zA-Z0-9]*$" | sed -e 's/.*\(\.[a-zA-Z0-9]*\)$/\1/' | sort | uniq -c | sort -n
```

- **Make the "tree" command pretty and useful by default**

```sh
    alias tree="tree -CAFa -I 'CVS|*.*.package|.svn|.git' --dirsfirst"
```

- **Find file on specific day**

```sh
    $ find ./ -type f -ls | grep 'jun'
```

- **Find executable files**

```sh
    $ find . -perm /a=x -type f
```

- **Find and count files with extention**

```sh
    $ find . -type f -name "*.php" | wc -l
```

- **Count all the lines of code in a directory recursively**

```sh
    $ find . -name '*.php' | xargs wc -l
```

- **Find modified files on especific day**

```sh
    $ find ./ -type f -ls | grep 'jun'

    #with exclude directory
    $ find ./ -type f ! -path "./.git/*" -ls | grep 'jun'
```

- **Find Dupicate files**

```sh
    $ find -not -empty -type f -printf "%s\n" | sort -rn | uniq -d | xargs -I{} -n1 find -type f -size {}c -print0 | xargs -0 md5sum | sort | uniq -w32 --all-repeated=separate

    # Duplicate Files
    $ sudo apt-get install -y fdupes

    $ fdupes -r .
```

- **Count Lines of Code - Using Cloc**

```sh
    $ sudo apt install -y cloc

    $ cloc .

    $ cloc --exclude-lang=DTD,Lua,make,Python .

    $ find . -name "*.php" | xargs cloc
```

- **Git Cloc**

```sh
    $ git clone https://github.com/kaelzhang/git-cloc.git

    $ cd git-cloc

    $ sudo make install

    Ex:
        git cloc -r
        git cloc
        git cloc --month 2014-6
```

- **Show users - home**

```sh
    $ cat /etc/passwd | grep "/home" |cut -d: -f1
```

- **Show users all and uid**

```sh
    $ awk -F":" '{ print "User: " $1 "\t\tuid:" $3 }' /etc/passwd
```

- **Show users all**

```sh
    % cat /etc/passwd | cut -d ":" -f1
```

- **wget**

```sh
    $ wget -r -l1 --no-parent -nH -nd -P/tmp -A".gif,.jpg,.png" http://example.com/images
```

- **Get External IP**

```sh
    $ curl http://ipecho.net/plain; echo

    $ lynx --dump http://ipecho.net/plain

    $ curl http://whatismyip.org/
```

- **Get Internal IP**

```sh
    $ /sbin/ifconfig eth0 | grep "inet addr" | awk -F: '{print $2}' | awk '{print $1}'
```

- **Todos los paquetes instaldados**

```sh
    $ dpkg --get-selections >> paquetes-instalados.txt

    $ grep install /var/log/dpkg.log >> paquetes-instalados.txt
```

## Open ports

- **Centos**

```sh
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

```sh
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

```sh
    # scp ~/.ssh/id_rsa.pub user@host:~/.ssh/authorized_keys
```

- **Upload Files SSH**

```sh
    $ scp FILE USER@SERVER:LOCATION
```

## rmate

```sh
    $ curl https://raw.github.com/aurora/rmate/master/rmate > rmate

    $ sudo mv rmate /usr/local/bin
        $  sudo mv rmate ~/.local/bin

    $ sudo chmod +x /usr/local/bin/rmate

    $ sudo iptables -A INPUT -p tcp --dport 52698 -j ACCEPT


```


## Download full website

```sh
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

```sh
    $ crontab -l
```

- View Users Cronjob

```sh
    $ crontab -u userName -l
    $ crontab -u vivek -l
```

- Install or create or edit my own cron jobs

```sh
    $ crontab -e
```

- Syntax of crontab

```sh
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

```sh
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

```sh
    $ touch ~/.xmodmap
    $ vim ~/.xmodmap
```

- Editar .xmodmap agregando:

```sh
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

```sh
    xmodmap -verbose ~/.xmodmap
```

## Otros comados utiles

- Ver teclas

```sh
    $ xmodmap -pke | less
```

- Ver las lista de dispositivos

```sh
    $ xinput list
```

- Diagnostico de las teclas

```sh
    $ xinput query-state 9
```

## Config Bandwidth

```sh
    $ sudo apt install -y trickle
```



## Montar Driver

```sh
    $ ll /dev/disk/by-uuid/ && ll /dev/disk/by-label/

    $ sudo sublime /etc/fstab

    +++ UUID=e2a5bf75-e511-4330-9f1e-efc114b9a47e /media/oo/Tera  ext4    errors=remount-ro 0       1

```


**Descargar MountManager**

```sh
    http://ubuntuforums.org/showthread.php?t=1604251
```

**Edit fstab**
```sh
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
    exec('tar -xzf SecretariaSalud.tar.gz',$ret);
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

- **Koala** - http://koala-app.com/
- **Pleeease** - http://pleeease.io/

# Alias

```sh
    alias = git ls-files -v | grep '^[[:lower:]]'
```
