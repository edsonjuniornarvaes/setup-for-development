# Configure machine for development
##### configure machine for development using ubuntu.

### Install chrome
```bash
$ wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
$ sudo dpkg -i google-chrome-stable_current_amd64.deb
```

### Install Gnome
:rocket: [Gnome](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep?hl=pt-BR)

```bash
$ sudo apt-get install -y gdebi gnome-tweak-tool gnome-shell-extensions chrome-gnome-shell
```

### Extensions Gnome 
:rocket: [Start overlay in application view](https://extensions.gnome.org/extension/1198/start-overlay-in-application-view/)  
:rocket: [Dash to dock](https://extensions.gnome.org/extension/307/dash-to-dock/)  
:rocket: [Alternate tab](https://extensions.gnome.org/extension/15/alternatetab/)  
:rocket: [Sound output device chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/)  
:rocket: [Remove panel app menu](https://extensions.gnome.org/extension/1084/remove-panel-app-menu/)  
:rocket: [Extend panel menu](https://extensions.gnome.org/extension/1201/extend-panel-menu/)  
:rocket: [Dash to panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)  
:rocket: [Scroll panel](https://extensions.gnome.org/extension/932/scroll-panel/)  
:rocket: [Transparent gnome panel](https://extensions.gnome.org/extension/1099/transparent-gnome-panel/)  
:rocket: [Bottom panel](https://extensions.gnome.org/extension/949/bottompanel/)  
:rocket: [Mmod panel](https://extensions.gnome.org/extension/898/mmod-panel/)  
:rocket: [Gnome shutdown button](https://extensions.gnome.org/extension/1056/gnome-shutdown-button/)  

### Install Icons
```bash
$ sudo add-apt-repository ppa: papirus / papirus
$ sudo apt install papirus-icon-theme
```

### Install Make

```bash
$ sudo apt-get update
$ sudo apt-get install make
```
### Install GIT
```bash
$ sudo apt-get install git
```

### Install PHP 

```bash
$ sudo apt install software-properties-common
$ sudo add-apt-repository ppa:ondrej/php
$ sudo apt update
$ sudo apt-get install php7.4-cli
$ sudo apt-get install php-gd php-xml php7.4-mbstring
```

### Install Composer
```bash
$ sudo apt update
$ sudo apt install php-cli unzip
$ cd ~
$ curl -sS https://getcomposer.org/installer -o composer-setup.php
$ sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```
### Test the installation
```bash
$ composer
```

### DBeaver
```bash
$ sudo add-apt-repository ppa:serge-rider/dbeaver-ce
$ sudo apt-get update
$ sudo apt-get install dbeaver-ce
```

### Composer

#### Check the version, in the following case is for versions greater than 20 of ubuntu.

### Docker
```bash
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
$ sudo apt update
$ apt-cache policy docker-ce
$ sudo apt install docker-ce
```
### Test the installation
```bash
$ sudo systemctl status docker
```

### Permission

```bash
$ sudo usermod -aG docker $(whoami)
$ sudo usermod -aG docker $USER
$ newgrp docker
```

### Docker Compose
```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
$ docker-compose --version
```

### Install NodeJS
```bash
$ sudo apt install nodejs
$ sudo apt install npm
```

### Install YARN
```bash
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
$ sudo apt-get update && sudo apt-get install yarn
$ sudo apt-get install --no-install-recommends yarn
$ yarn --version
```
