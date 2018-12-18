# Install Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

# Install Cask
```
brew tap caskroom/cask
```

# Install tools
```
# Tools
brew install git

# For RAMAS/Java projects
brew install maven

# Frontend development
brew install nvm node yarn

# Other stuff I installed
brew install jq # Quick JSON parsing
```

# zsh
If you want to use zsh instead of bash, here's a few directions/links

```
brew install zsh zsh-completions # Use ZSH instead of bash
```

- [Oh my ZSH](https://github.com/robbyrussell/oh-my-zsh)


# Install Cask tools
```
# For Ramas
brew cask install caskroom/versions/java8
brew cask install docker eclipse-java pgadmin4 

# Communication
brew cask install slack

# Other stuff (Install if needed)
brew cask install iterm2 google-chrome pycharm-ce vagrant virtualbox visual-studio-code
```

### In order to use the above tools with the setup you must open them first

# Google Cloud SDK
## Install
```
curl https://sdk.cloud.google.com | bash
exec -l $SHELL
gcloud init
gcloud config set project resson-1208
```
[Ref](https://cloud.google.com/sdk/downloads)


## Login
```
gcloud auth login

gcloud components install docker-credential-gcr
docker-credential-gcr configure-docker
```

### If for some reason the oauth flow with gcloud auth login fails, use the following flag to manually pass the token to the terminal
```
gcloud auth login --no-launch-browser
```


# Setup Github
[Setup github SSH Credentials](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

# Setup Resson Google Account
- Mail (Apple Mail)
- Calendar (Apple Calendar)

# RAMAS
Quick summary below, more detailed summary in [the README](https://github.com/RessonAerospace/ramas)

## Clone
```
git clone git@github.com:RessonAerospace/ramas.git
cd ramas
```

## Run API Locally from docker-compose
```
docker-compose up -d api
```

## Build API Locally
```
mvn clean package
```

## Import into eclipse
Add Update Library `http://download.eclipse.org/tools/ajdt/47/dev/update` and install all packages within it.

`Import -> Existing Maven Project` and import `ramas-parent` and all subprojects