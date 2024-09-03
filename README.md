# macOSFrontend Development Setup

This guide will walk you through the setup of essential tools for frontend development on your new macOS machine.

## Table of Contents
- [Installing Homebrew](#installing-homebrew)
- [Installing Zsh and Oh My Zsh](#installing-zsh-and-oh-my-zsh)
- [Installing NVM (Node Version Manager)](#installing-nvm-node-version-manager)
- [Installing Browsers](#installing-browsers)
- [Setting Up Git](#setting-up-git)
- [Installing VS Code](#installing-vs-code)
- [Installing Additional Tools](#installing-additional-tools)

## Installing Homebrew

Homebrew is the package manager for macOS. It allows you to install and manage software packages easily.

### Step 1: Install Homebrew

Open the Terminal and run the following command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Step 2: Add Homebrew to your PATH

After installation, follow the on-screen instructions to add Homebrew to your PATH. Typically, this involves adding the following line to your `~/.zshrc` or `~/.bash_profile`:

```sh
export PATH="/opt/homebrew/bin:$PATH"
```

Reload your terminal with:

```sh
source ~/.zshrc
```

## Installing Zsh and Oh My Zsh

Zsh is a powerful shell, and Oh My Zsh is a delightful open-source framework for managing your Zsh configuration.

### Step 1: Install Zsh (if not already installed)

macOS comes with Zsh pre-installed, but you can install it via Homebrew to ensure you have the latest version:

```sh
brew install zsh
```

### Step 2: Install Oh My Zsh

Install Oh My Zsh using the following command:

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Step 3: Set Zsh as Default Shell

You can set Zsh as your default shell by running:

```sh
chsh -s $(which zsh)
```

## Installing NVM (Node Version Manager)

NVM allows you to manage multiple versions of Node.js on your machine.

### Step 1: Install NVM via Homebrew

Run the following command to install NVM:

```sh
brew install nvm
```

### Step 2: Configure NVM

Create a directory for NVM and add it to your shell profile:

```sh
mkdir ~/.nvm
echo "export NVM_DIR=~/.nvm" >> ~/.zshrc
echo "source $(brew --prefix nvm)/nvm.sh" >> ~/.zshrc
```

Reload your terminal:

```sh
source ~/.zshrc
```

### Step 3: Install Node.js

Now you can install the latest version of Node.js with:

```sh
nvm install node
```

You can also install specific versions with:

```sh
nvm install <version>
```

## Installing Browsers

As a frontend developer, having multiple browsers for testing is essential. You can install Chrome, Firefox, Edge, and Brave via Homebrew.

### Step 1: Install Browsers

Run the following commands to install each browser:

```sh
brew install --cask google-chrome
brew install --cask firefox
brew install --cask microsoft-edge
brew install --cask brave-browser
```

## Setting Up Git

Git is a version control system that is widely used in development.

### Step 1: Install Git

Git comes pre-installed on macOS, but you can update it via Homebrew:

```sh
brew install git
```

### Step 2: Configure Git

Set up your global Git configuration:

```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Installing VS Code

Visual Studio Code is a popular code editor for frontend development.

### Step 1: Install VS Code

Install VS Code via Homebrew:

```sh
brew install --cask visual-studio-code
```

### Step 2: Install VS Code Extensions

Some useful extensions for frontend development include:

- Prettier - Code formatter
- ESLint - Linting JavaScript
- Live Server - Launch a development local server with live reload feature
- GitLens - Git supercharged

You can install these directly within the VS Code Extensions Marketplace.

## Installing Additional Tools

Here are some additional tools that you might find useful:

### Step 1: Install Yarn (alternative package manager to npm)

```sh
brew install yarn
```

### Step 2: Install HTTP Server (for serving static files)

```sh
npm install -g http-server
```

### Step 3: Install ImageMagick (for image processing)

```sh
brew install imagemagick
```

### Step 4: Install Docker (for containerization)

```sh
brew install --cask docker
```

### Step 5: Install Postman (for API testing)

```sh
brew install --cask postman
```

## Conclusion

With these tools installed, your macOS M3 machine is now ready for frontend development. Happy coding!
