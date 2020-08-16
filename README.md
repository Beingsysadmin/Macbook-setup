# Macbook-setup

I thought I would take some time and document what I do when I get a new machine and put all of my steps , so that it will be easier for me to track and update.

First Time Setup
The first thing you should do is update your system. To do that go: Apple menu () > About This Mac > Software Update. Also upgrade your OS to the latest version to have a more secure OS. macOS upgrades are usually free so you might as well keep your machine up to date.

# Getting Started

* HomeBrew:

Homebrew calls itself The missing package manager for macOS and is an essential tool for any developer.

Before you install HomeBrew though you need to install the xcode command line utilities. Open up a new terminal and type the following command.
```
xcode-select --install
```
It'll prompt you to install the command line tools. Follow the instructions and you'll have Xcode and Xcode command line tools both installed.

HomeBrewInstallation:

To install Homebrew run the following in a terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

```
Post Installation

If you need help with brew you can run brew help.
```
brew update - You shouldn't have anything to update but its good to check.
brew search 'term' to search for brews
```

* iTerm2

I am now using iTerm2 full time and I absolutely love it and good replace for default Terminal in mac.

```
brew cask install iterm2
```
* ohmyzsh

"Configuring Oh My ZSH"
```
 curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sH
```
"Configure ZSH  plugins"
```
 git clone git://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
 git clone https://github.com/zsh-users/zsh-syntax-highlighting ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
 sed -i 's/plugins=(git)/plugins=(\n  git\n)/g' ~/.zshrc
 sed -i 's/git$/git\'$'\n  zsh-autosuggestions/g' ~/.zshrc
 sed -i 's/zsh-autosuggestions$/zsh-autosuggestions\'$'\n  zsh-syntax-highlighting/g' ~/.zshrc
```

# Development Setup
Now that I have a nice looking command line full of features its time to start installing all of the different applications I will use. If you have any questions about any of these or why I install them please see the contact me section below.
```
brew install git
brew cask install google-chrome
brew cask install brave-browser
brew cask install visual-studio-code
brew cask install intellij-idea
brew cask install eclipse-java
brew cask install postman
brew cask install docker
brew install tree
brew cask install atom
brew tap jenkins-x/jx
brew cask install google-cloud-sdk
brew cask install zoomus
brew install terraform
brew install node
brew install python
brew install jq
brew install kops
brew install kafka
brew install tmux
brew install kubectl
brew install helm
```

# Git Config
 We used brew to install the latest earlier. Now that we are on the latest version of git we need to do a little configuration.

* Configure git
```
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"
git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status

```

# Visual Studio Code
 One of the MSFT great product and dev's most popular choice.

* Extensions

If you want to get a list of extensions currently installed on your machine you can use the following command.
```
code --list-extensions

code --install-extension ${extension-name} - The nice thing about that is you can install visual studio code extensions using the command line.
```
* Configure VS Code extensions

```
code    --install-extension ms-azuretools.vscode-docker \
        --install-extension marcostazi.VS-code-vagrantfile \
        --install-extension mauve.terraform \
        --install-extension secanis.jenkinsfile-support \
        --install-extension formulahendry.code-runner \
        --install-extension mikestead.dotenv \
        --install-extension oderwat.indent-rainbow \
        --install-extension orta.vscode-jest \
        --install-extension jenkinsxio.vscode-jx-tools \
        --install-extension mathiasfrohlich.kotlin \
        --install-extension christian-kohler.npm-intellisense \
        --install-extension sujan.code-blue \
        --install-extension waderyan.gitblame \
        --install-extension ms-vscode.go \
        --install-extension in4margaret.compareit \
        --install-extension andys8.jest-snippets \
        --install-extension euskadi31.json-pretty-printer \
        --install-extension yatki.vscode-surround \
        --install-extension wmaurer.change-case
```
# SDKMan
This is one of my favorite version managers because I use a lot of the Software Development Kits (SDKs) it manages. If you haven't heard of SDKMan check them out here. This is a list of SDKs I manage using SDKMan.

Java
Groovy
Grails
Gradle
Maven
Micronaut
Spring Boot

Here is a full list of SDKs https://sdkman.io/sdks
Installation: curl -s "https://get.sdkman.io" | bash

If you just type sdk install candidate it will install the latest stable version or you can install a specific version

```
sdk install java 8.0.191-oracle
If you need to get a list of versions you can ask for it:
sdk list java

```
# Browser Configuration
Turn on sync and sign into chrome, this brings all of my bookmarks and extensions.

* Extensions
```
LastPass
Grammarly
oneTab
JSONViewer

```

# Have fun
```
brew install cowsay ponysay fortune lolcat
fortune | ponysay
#or
fortune | cowsay | lolcat

```
* figlet

  ```
  brew install figlet
  ```

```
MacBook-Pro Macbook-setup % figlet macbook set up
                      _                 _               _
 _ __ ___   __ _  ___| |__   ___   ___ | | __  ___  ___| |_   _   _ _ __
| '_ ` _ \ / _` |/ __| '_ \ / _ \ / _ \| |/ / / __|/ _ \ __| | | | | '_ \
| | | | | | (_| | (__| |_) | (_) | (_) |   <  \__ \  __/ |_  | |_| | |_) |
|_| |_| |_|\__,_|\___|_.__/ \___/ \___/|_|\_\ |___/\___|\__|  \__,_| .__/
                                                                   |_|
                                                                   ```
