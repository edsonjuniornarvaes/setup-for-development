# Configure machine for development
##### configure machine for development using ubuntu version 18.

### install gnome
[Gnome](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep?hl=pt-BR)

```bash
$ sudo apt-get install -y gdebi gnome-tweak-tool gnome-shell-extensions chrome-gnome-shell
```

### extensions gnome 
[Start overlay in application view](https://extensions.gnome.org/extension/1198/start-overlay-in-application-view/)
[Dash to dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
[Alternate tab](https://extensions.gnome.org/extension/15/alternatetab/)
[Sound output device chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/
[Remove panel app menu](https://extensions.gnome.org/extension/1084/remove-panel-app-menu/)
[Extend panel menu](https://extensions.gnome.org/extension/1201/extend-panel-menu/)
[Dash to panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)
[Scroll panel](https://extensions.gnome.org/extension/932/scroll-panel/)
[Transparent gnome panel](https://extensions.gnome.org/extension/1099/transparent-gnome-panel/)
[Bottom panel](https://extensions.gnome.org/extension/949/bottompanel/)
[Mmod panel](https://extensions.gnome.org/extension/898/mmod-panel/)
[Dash to panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)
[Gnome shutdown button](https://extensions.gnome.org/extension/1056/gnome-shutdown-button/)

### Ícons
```bash
$ wget -qO- https://raw.githubusercontent.com/PapirusDevelopmentTeam/papirus-icon-theme/master/install.sh | DESTDIR="$HOME/.icons" sh
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
```
```bash
$ sudo add-apt-repository ppa:ondrej/php
```
```bash
$ sudo apt update
```
```bash
$ sudo apt-get install php7.2-cli
```
```bash
$ sudo apt-get install php7.4-cli
```
```bash
$ sudo apt-get install php-gd php-xml php7.4-mbstring
```

### Install composer
```bash
$ sudo apt install wget php-cli php-zip unzip
```
```bash
$ php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
```
```bash
$ HASH="$(wget -q -O - https://composer.github.io/installer.sig)"
```
```bash
$ php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
```
```bash
$ sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```

### Composer

### install docker
```bash
$ sudo apt update
```
```bash
$ sudo apt upgrade
```
```bash
$ sudo apt-get install curl apt-transport-https ca-certificates software-properties-common
```
```bash
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```bash
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
```bash
$ sudo systemctl status docker
```
```bash
$ sudo systemctl status docker
```
```bash
$ docker ps
```
```bash
$ permissao
```
```bash
$ sudo usermod -aG docker $(whoami)
```
```bash
$ sudo usermod -aG docker $USER
```
```bash
$ newgrp docker
```

### Docker compose
```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```bash
$ sudo chmod +x /usr/local/bin/docker-compose
```
```bash
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```
```bash
$ docker-compose --version
```

### Install apache2
> var/www/html
[Instalar apache](https://matheuslima.com.br/instalando-o-apache-php-74-mysql-lamp)
```bash
$ sudo chmod 777 -R html
```
```bash
$ sudo apt-get install apache2 
```
```bash
$ libapache2-mod-php7.3
```
### NodeJS
[Instalar node](https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/)
```bash
$ sudo apt install nodejs
```
```bash
$ sudo apt install npm
```
```bash
$ sudo apt remove nodejs
```
```bash
$ sudo npm cache clean --force
```
```bash
$ sudo chown -R $USER /usr/local/lib
```
```bash
$ sudo npm install -g typescript
```

### YARN
```bash
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
```
```bash
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```
```bash
$ sudo apt-get update && sudo apt-get install yarn
```
```bash
$ sudo apt-get install --no-install-recommends yarn
```
```bash
$ yarn --version
```
