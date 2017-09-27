# linux-setup
My linux Setup 😛

## OS

 I use Ubuntu Gnome 16.04, plus [Adapta GTK theme](https://github.com/adapta-project/adapta-gtk-theme/) and [Papirus Icons](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme/)


## Config Steps

#### Theme
##### Adapta GTK installation
You will need to add the repository to your system sources list before installing it:

```
sudo add-apt-repository ppa:tista/adapta
sudo apt update
sudo apt install adapta-gtk-theme
```

##### Papyrus Icons
Similarly, you will have to add the Paper Project repo:

```
sudo add-apt-repository ppa:papirus/papirus
sudo apt-get update
sudo apt-get install papirus-icon-theme
```

##### Activating all
Open the Gnome Tweak Tool from the Applications list or from the terminal with the command `gnome-tweak-tool`. In the tab *Appearance*, choose *Adapta* (or variants) from the GTK+ dropdown, and *Papyrus* from the *Icons* one. Done, you are themed

### Hyper shell terminal

I use the [Hyper Shell] (https://hyper.is/) as my main terminal and some plugins to make it better 😛

you can check some others plugin at [this repo] (https://github.com/bnb/awesome-hyper)

to install plugins, just edit the `~/hyper.js` file and add the name of the plugins like this :
```
plugins: [
  "hyperline",
  "hyper-materialshell",
  "hyper-statusline",
  "hyper-tabs-enhanced"
]
```

### Aliases

I use som aliases to make thing better.

here are someones :
```bash
#
alias c="clear"
# if user is not root, pass all commands via sudo #
if [ $UID -ne 0 ]; then
    alias reboot='sudo reboot'
    alias shutdown='sudo shutdown'
    alias update='sudo apt update && sudo apt upgrade'
fi

## get rid of command not found ##
alias cd..='cd ..'

## a quick way to get out of current directory ##
alias ..='cd ..'
alias ...='cd ../../../'
alias ....='cd ../../../../'
alias .....='cd ../../../../'
alias .4='cd ../../../../'
alias .5='cd ../../../../..'

## pass options to free ##
alias meminfo='free -m -l -t'

## get top process eating memory
alias psmem='ps auxf | sort -nr -k 4'
alias psmem10='ps auxf | sort -nr -k 4 | head -10'

## get top process eating cpu ##
alias pscpu='ps auxf | sort -nr -k 3'
alias pscpu10='ps auxf | sort -nr -k 3 | head -10'

## Get server cpu info ##
alias cpuinfo='lscpu'

## get GPU ram on desktop / laptop##
alias gpumeminfo='grep -i --color memory /var/log/Xorg.0.log'
```

yo can edit/create a file called `.bash_aliases` and write there your custom alias

### Visual Studio Code
You may get the VSCode from its official site: https://code.visualstudio.com/


## bye!
Hope you can find some usefulness in this setup! If you want to give a hello, shout out, my Twitter is [@carlosRGL](https://twitter.com/Carlosrgl_88). See you!