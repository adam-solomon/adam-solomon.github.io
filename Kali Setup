# Kali Linux Setup

This is a list of commands and stuff to install on a Kali 2020.2 installation. Kali comes with many pre-installed applications and services, but I install a lot of extra tools for CTF's and pen test engagements.

## 4k / High DPI Monitor Configuration

Scaling is a pain when using VirtualBox on a 4k monitor. This article will outline the exact steps needed to setup scaling properly on a high DPI 4k monitor:

https://www.kali.org/docs/general-use/hidpi/

## Package Managed Software

**Using Apt:**

```
sudo apt install filezilla
sudo apt install gobuster
sudo apt install jxplorer
sudo apt install python3-pip
```

**Using Gem:**

```
sudo gem install evil-winrm
```

**Using Pip3:**

```
sudo pip3 install bloodhound
```

## Sysinternals

Download this ZIP file and extract it somewhere so the tools are easily available.

https://download.sysinternals.com/files/SysinternalsSuite.zip

## Chisel

Chisel provides an easy way to setup tunneling and SOCKS5 proxies on hosts and networks.

```
curl https://i.jpillora.com/chisel\! | bash
```

## Git Repos

These are various tools I like to use that can be cloned from Git. I prefer to put everything in the `/opt` directory.

- https://github.com/danielmiessler/SecLists
- https://github.com/irsdl/iis-shortname-scanner/
- https://github.com/andrew-d/static-binaries
- https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite
- https://github.com/NotMedic/NetNTLMtoSilverTicket/
- https://github.com/evilmog/ntlmv1-multi
- https://github.com/internetwache/GitTools

## Docker

Once in a while a Docker container is needed to run apps, especially when stuff breaks (*I'm looking at you Bloodhound*).

```
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
echo 'deb [arch=amd64] https://download.docker.com/linux/debian buster stable' | sudo tee /etc/apt/sources.list.d/docker.list

sudo apt update
sudo apt remove docker docker-engine docker.io
sudo apt install docker-ce -y

sudo systemctl start docker
```

## Fonts

Oh My Zsh themes may require Powerline fonts.

```
sudo apt-get install fonts-powerline
```

## Oh My Zsh

Oh My Zsh is an amazing shell which provides a much nicer experience than the old fashioned Linux shells like Bash.

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

**Aphrodite Theme**

I like this theme, but there's a lot out there to choose from. Do this with the "kali" and "root" users, unless you want the shells to look different.

```
mkdir -p ~/.oh-my-zsh/custom/themes/
wget -xqO ~/.oh-my-zsh/custom/themes/aphrodite.zsh-theme https://git.io/v5ohc
sed -i.bak 's/^[[:space:]]*ZSH_THEME=.*/ZSH_THEME="aphrodite"/' ~/.zshrc
source ~/.zshrc 
```

## Firefox Extensions

**Wappalyzer** - Easily detects web app software in use.

**FoxyProxy Standard** - Allows for easy switching between no proxy and something like a Burp proxy.
