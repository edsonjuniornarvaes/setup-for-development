# Configure machine for development
##### configure machine for development using ubuntu version 18.

### Install gnome
:rocket: [Gnome](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep?hl=pt-BR)

```bash
$ sudo apt-get install -y gdebi gnome-tweak-tool gnome-shell-extensions chrome-gnome-shell
```

### extensions gnome 
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
:rocket: [Dash to panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)  
:rocket: [Gnome shutdown button](https://extensions.gnome.org/extension/1056/gnome-shutdown-button/)  

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

// ==UserScript==
// @name        GitHub Copy Code Snippet
// @version     0.3.6
// @description A userscript adds a copy to clipboard button on hover of markdown code snippets
// @license     MIT
// @author      Rob Garrison
// @namespace   https://github.com/Mottie
// @include     https://github.com/*
// @include     https://gist.github.com/*
// @run-at      document-idle
// @grant       GM_addStyle
// @require     https://greasyfork.org/scripts/28721-mutations/code/mutations.js?version=666427
// @icon        https://github.githubassets.com/pinned-octocat.svg
// @updateURL   https://raw.githubusercontent.com/Mottie/GitHub-userscripts/master/github-copy-code-snippet.user.js
// @downloadURL https://raw.githubusercontent.com/Mottie/GitHub-userscripts/master/github-copy-code-snippet.user.js
// ==/UserScript==
(() => {
	"use strict";

	let copyId = 0;
	const markdownSelector = ".markdown-body, .markdown-format",
		codeSelector = "pre:not(.gh-csc-pre)",

		copyButton = document.createElement("clipboard-copy");
	copyButton.className = "btn btn-sm tooltipped tooltipped-w gh-csc-button";
	copyButton.setAttribute("aria-label", "Copy to clipboard");
	// This hint isn't working yet (GitHub needs to fix it)
	copyButton.setAttribute("data-copied-hint", "Copied!");
	copyButton.innerHTML = `
		<svg aria-hidden="true" class="octicon octicon-clippy" height="16" viewBox="0 0 14 16" width="14">
			<path fill-rule="evenodd" d="M2 13h4v1H2v-1zm5-6H2v1h5V7zm2 3V8l-3 3 3 3v-2h5v-2H9zM4.5 9H2v1h2.5V9zM2 12h2.5v-1H2v1zm9 1h1v2c-.02.28-.11.52-.3.7-.19.18-.42.28-.7.3H1c-.55 0-1-.45-1-1V4c0-.55.45-1 1-1h3c0-1.11.89-2 2-2 1.11 0 2 .89 2 2h3c.55 0 1 .45 1 1v5h-1V6H1v9h10v-2zM2 5h8c0-.55-.45-1-1-1H8c-.55 0-1-.45-1-1s-.45-1-1-1-1 .45-1 1-.45 1-1 1H3c-.55 0-1 .45-1 1z"></path>
		</svg>`;

	GM_addStyle(`
		.gh-csc-wrap {
			position: relative;
		}
		.gh-csc-wrap:hover .gh-csc-button {
			display: block;
		}
		.gh-csc-button {
			display: none;
			padding: 3px 6px;
			position: absolute;
			top: 3px;
			right: 3px;
			z-index: 20;
		}
		.gh-csc-wrap.ghd-code-wrapper .gh-csc-button {
			right: 31px;
		}
		.gh-csc-button svg {
			vertical-align: text-bottom;
		}
	`);

	function addButton(wrap, code) {
		if (!wrap.classList.contains("gh-csc-wrap")) {
			copyId++;
			// See comments from sindresorhus/refined-github/issues/1278
			code.id = `gh-csc-${copyId}`;
			copyButton.setAttribute("for", `gh-csc-${copyId}`);
			wrap.classList.add("gh-csc-wrap");
			wrap.insertBefore(copyButton.cloneNode(true), wrap.childNodes[0]);
		}
	}

	function init() {
		const markdown = document.querySelector(markdownSelector);
		if (markdown) {
			[...document.querySelectorAll(markdownSelector)].forEach(md => {
				[...md.querySelectorAll(codeSelector)].forEach(pre => {
					let code = pre.querySelector("code");
					let wrap = pre.parentNode;
					if (code) {
						// pre > code
						addButton(pre, code);
					} else if (wrap.classList.contains("highlight")) {
						// div.highlight > pre
						addButton(wrap, pre);
					}
				});
			});
		}
	}

	document.addEventListener("ghmo:container", init);
	document.addEventListener("ghmo:comments", init);
	init();
})();
