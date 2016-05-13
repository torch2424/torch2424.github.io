---
layout: guide
category: guide
title: Elementary OS / Ubuntu Initial Dev Install
shortDescription: A guide on getting started with a fresh Elementary OS or Ubuntu install
---

(Last Updated: 7/12/15)
(Last OS Tested by Torch2424: Elementary OS Freya [Built on Ubuntu 14.04])

A simple Readme.md on my personal instructions on how to set up an Elementary OS laptop with modern Web Development in mind. This is part One of a web development install series.

# These Guides Are Useful, but could be done better

I have recently discovered/understood [Vagrant](https://www.vagrantup.com/docs/getting-started/) which allows you to create virtual development environments. Because of this, if anything breaks, you can easily destroy the environment, and start over, without having to re-install your entire machine from scratch. It's awesome, and also allows for sharing your vagrant box to others through a URL, and all sorts of cool features! I highly reccomend that you take the time to learn it, or take a look at it!

[I have a repo with all of my vagrant files](https://github.com/torch2424/vagrantBoxes), so if you would like an easy way to make this environment in vagrant, I currently have it under the folder "WebDevJSRuby", which will give you an up-to-date version of this guide.

If you prefer doing it yourself, the original guide is below...

Thank you!

---

# This is simply a list of terminal Commands for Ubuntu/Elementary

## Initial Upgrade

```
sudo apt-get update && sudo apt-get upgrade
```

This will update everything to the newest packages

## Add some third-party package repos

```
sudo add-apt-repository ppa:mpstark/elementary-tweaks-daily

sudo add-apt-repository ppa:linrunner/tlp

sudo apt-add-repository -y ppa:teejee2008/ppa

sudo apt-add-repository ppa:numix/ppa

sudo add-apt-repository ppa:moka/stable
```

Install these at your own discretion, and you may have to enter them one at a time

Elementary tweaks - Awesome extension to the settings app, letting you tweak a lot of look and feel

TLP (Laptops) - This saves your laptop battery as it checks if you are running on battery or plugged in, and scales your performance accordingly. This is a HUGE battery saver for me and I love it

teejee008/Conky manager - and easy to use conky manager to make a nice looking conky set up

numix/moka - Beautiful icon packs for elementary/ubuntu


## Update again

```
sudo apt-get update
```

Now that you've added these new repos. We should update them to see their newest versions!

## Install The Apps!

Depending on your needs you may not need all of these, but these are my personal apps I always install. You can easily pick and choose

```
sudo apt-get install ubuntu-restricted-extras elementary-tweaks git vlc libreoffice firefox gdebi transmission gimp rar tlp tlp-rdw numix-icon-theme-circle steam conky conky-manager openjdk-7-jdk faba-icon-theme moka-icon-theme gparted
```

Awwweeee yes. Some good ol' apps for your fancy computer, I'll run this down on what each does

ubuntu-restricted-extras - this will give you support for many random things like .mp3 and video files, that are normally under some weird copy right thingy

elementary-tweaks - described above, you'll need the repos

git - Git literally changed my life. I posted this readme using git. It's version control for code, and it's how we will post to github

vlc - the best video player with A LOT of support for different video files

libreoffice - An open source office suit for linux, great for students or anyone doing office work

firefox - A great web browser, I always install because you never know when chrome will go down

debi - A very awesome, fast, and easy .deb package installer, much better than the software suite

transmission - a very good torrent program for linux, quite popular

gimp - an open source photoshop-like image editor

rar - gives support for .rar files, because not everything is in a .zip

tlp - you'll need the repo, see above

tlp-rdw - you'll need the repo, see above

numix-icon-theme-circle - you'll need the repo, see above

steam - A great game distribution service, one day they realized the Linux/Ubuntu  were master race, and ported it to linux! Now you can download most of your favorite indie games and play them on your machine!

conky - An awesome stats monitor that sits on your desktop, and highly themeable/hackable

conky-manager - you'll need the repo, see above

openjdk-7-jdk - The java development kit. It'll also install the jre (java runtime environment), you'll need to run java apps, like minecraft, or develop apps for android

faba-icon-theme - Another Awesome Icon theme, I think it's also linked to one of the repos above

moka-icon-theme - you'll need the repo, see above

gparted - awesome partition management, it's saved me quite a few times!

## Get TLP started (Laptops)!

```
sudo tlp start
```

You should only have to do this once, after this, TLP will automatically start on the OS startup, for all the awesome battery savings


## Get Some Debs!

I suggest getting google chrome, dropbox, and atom (You can do this with wget, but I'd rather just use a browser haha)

Google Chrome: https://www.google.com/chrome/browser/desktop/

Dropbox: https://www.dropbox.com/install?os=lnx

Atom: https://atom.io/

Google Chrome is arguably the best desktop web browser, and it's my one of choice (I suggest the beta version, tends to work better on Elementary). Dropbox is an awesome cloud storage solution, I highly recommend it, I find it better than google drive actually, and I'm a Google die-hard. And lastly, Atom is THE best text editor, specifically for web development.

## Fix Double Chrome Icons (Chrome & Elementary OS)!

http://itsfoss.com/rid-google-chrome-icons-dock-elementary-os-freya/

On Elementary OS, chrome has this weird double icon bug that can be fixed above!

## Set Up A Web Development Environment (Web Developers)!

I created another repo on setting up a web development environment that's treated me very well for a while now, And I try to keep it updated!

https://github.com/torch2424/Elementary-Ubuntu-Web-Dev-Environment


## THE END!

Thanks for Reading through my guide! I hope it helped, and feel free to commit or submit any pull requests! Star the repo if you liked it, and don't be afraid to follow me, I'll probably follow back haha! Thanks!
