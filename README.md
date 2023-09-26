
# Tools

I guess you are already using iTerm2. If you are not, start by installing it [iterm2.com](https://iterm2.com) and use that instead of terminal.

Also another tool that we will need in the journey is homebrew ([brew.sh](https://brew.sh)). If you dont already have it, just install it by:

```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```

after the installed is done, you need to execute a couple of lines to add it to your path:

```
➜  ~   (echo; echo 'eval "$(/usr/local/bin/brew shellenv)"') >> /Users/ivan/.zprofile
➜  ~   eval "$(/usr/local/bin/brew shellenv)"
```

a third tool to keep in consideration are Apple Xcode tools. Do:

```
 sudo rm -rf /Library/Developer/CommandLineTools
 sudo xcode-select --install
```
and accept the license pop-up

# Framework

Then next thing to consider is the installation of a framework. Here we chose OhMyZsh (). Execute the following:

```sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"```

![Oh-My-Zsh](image-1.png)

Let's add some customisation for the prompt with powerlevel10k [P10k](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k). If you just run:

```
brew install powerlevel10k
echo "source $(brew --prefix)/share/powerlevel10k/powerlevel10k.zsh-theme" >>~/.zshrc
```
... and then close the terminal window and open a new one, and follow the on screen menu for customising the prompt to match your likes. It will be important later on to indicate the cluster and namespace in which you are working. You can always use defaults if you dont have a personal preference on something. Usually first line is the typical choice.

![restart iTerm2](image.png)

And now, lets add some plugins to make typing easier. They are all [here](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins), but recommended at least are:



