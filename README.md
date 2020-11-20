# Configure machine for development
##### configure machine for development using ubuntu version 18.

### install gnome
:rocket: [Gnome](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep?hl=pt-BR)

```bash
$ sudo apt-get install -y gdebi gnome-tweak-tool gnome-shell-extensions chrome-gnome-shell
```

### extensions gnome 
:rocket: [Start overlay in application view](https://extensions.gnome.org/extension/1198/start-overlay-in-application-view/)··
:rocket: [Dash to dock](https://extensions.gnome.org/extension/307/dash-to-dock/)··
:rocket: [Alternate tab](https://extensions.gnome.org/extension/15/alternatetab/)··
:rocket: [Sound output device chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/)··
:rocket: [Remove panel app menu](https://extensions.gnome.org/extension/1084/remove-panel-app-menu/)··
:rocket: [Extend panel menu](https://extensions.gnome.org/extension/1201/extend-panel-menu/)··
:rocket: [Dash to panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)··
:rocket: [Scroll panel](https://extensions.gnome.org/extension/932/scroll-panel/)··
:rocket: [Transparent gnome panel](https://extensions.gnome.org/extension/1099/transparent-gnome-panel/)··
:rocket: [Bottom panel](https://extensions.gnome.org/extension/949/bottompanel/)··
:rocket: [Mmod panel](https://extensions.gnome.org/extension/898/mmod-panel/)··
:rocket: [Dash to panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)····
:rocket: [Gnome shutdown button](https://extensions.gnome.org/extension/1056/gnome-shutdown-button/)··

### Ícons
```bash
$ sudo add-apt-repository ppa:varlesh-l/papirus-pack -y && sudo apt-get update && sudo apt-get install papirus-gtk-icon-theme -y
```

### Install make

```bash
$ sudo apt-get update
```
```bash
$ sudo apt-get install make
```
### Install GIT
```bash
$ sudo apt-get install git
```

### Install php 

```bash
$ sudo apt install software-properties-common
$ sudo add-apt-repository ppa:ondrej/php
$ sudo apt update
$ sudo apt-get install php7.4-cli
$ sudo apt-get install php-gd php-xml php7.4-mbstring
```

### Install composer
```bash
$ sudo apt install wget php-cli php-zip unzip
$ php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
$ HASH="$(wget -q -O - https://composer.github.io/installer.sig)"
$ php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
$ sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```

### Composer

### install docker
```bash
$ sudo apt update
$ sudo apt upgrade
$ sudo apt-get install curl apt-transport-https ca-certificates software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
$ sudo systemctl status docker
$ docker ps
```

### Permission

```bash
$ sudo usermod -aG docker $(whoami)
$ sudo usermod -aG docker $USER
$ newgrp docker
```

### Docker compose
```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
$ docker-compose --version
```

### Install apache2
> var/www/html

:rocket: [Instalar apache](https://matheuslima.com.br/instalando-o-apache-php-74-mysql-lamp)

```bash
$ sudo chmod 777 -R html
$ sudo apt-get install apache2 
$ libapache2-mod-php7.3
```
### NodeJS
:rocket: [Instalar node](https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/)
```bash
$ sudo apt install nodejs
$ sudo apt install npm
```

### YARN
```bash
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
$ sudo apt-get update && sudo apt-get install yarn
$ sudo apt-get install --no-install-recommends yarn
$ yarn --version
```
