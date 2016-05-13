---
layout: guide
category: guide
title: Elementary OS / Ubuntu Web Dev Install
shortDescription: A guide on installing a web developer environment on Elementary OS / Ubuntu
---

Part One:
http://blog.aaronthedev.com/initial-dev-install/

(Last Updated: 7/12/15)
(Last OS Tested by Torch2424: Elementary OS Freya [Built on Ubuntu 14.04])

A simple Readme.md on how to set up a web development environment in Ubuntu or Elementary OS. Part two of the series.

# These Guides Are Useful, but could be done better

I have recently discovered/understood [Vagrant](https://www.vagrantup.com/docs/getting-started/) which allows you to create virtual development environments. Because of this, if anything breaks, you can easily destroy the environment, and start over, without having to re-install your entire machine from scratch. It's awesome, and also allows for sharing your vagrant box to others through a URL, and all sorts of cool features! I highly reccomend that you take the time to learn it, or take a look at it!

[I have a repo with all of my vagrant files](https://github.com/torch2424/vagrantBoxes), so if you would like an easy way to make this environment in vagrant, I currently have it under the folder "WebDevJSRuby", which will give you an up-to-date version of this guide.

If you prefer doing it yourself, the original guide is below...

Thank you!

---

This guide was created with the help of Yeoman: http://yeoman.io/codelab/setup.html and npm no sudo: https://github.com/glenpike/npm-g_nosudo

#This is simply a list of terminal Commands for Ubuntu/Elementary, with some cool links you can click

##Install some initial modern web dev packages

```
sudo apt-get install nodejs npm git
```

This will install a few packages:

nodejs - THE awesome new service that is used to code backend in javascript, and is required by most web dev packages.

npm - npm is an awesome package manager for packages specifically meant for web development

git - (We installed this in part one, it's okay to run again, does no harm) Git literally changed my life. I posted this readme using git. It's version control for code, and it's how we will post to github


##Create a symbolic link to get things working

```
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

This will create a symbolic link for nodejs, which will allow it to work! I honestly forgot where I found that you should use this, but it always works for me!

##Update Node!

```
curl -sL https://deb.nodesource.com/setup_0.12 | sudo bash -


sudo apt-get install -y nodejs
```

Two seperate commands, the first will get a more recent nodejs source we can update our node from (Since Ubuntu doesn't always have the most up to date repos), the second will install nodejs to it's newest version!

##Make sure eveything installed correctly!

```
node -v

npm -v

git --version
```

This will return all the versions of things we just installed, if one of them doesn't returna  version, you should go back and try to re-install, and make sure node has the newest version if not very recent

##Install Ruby!

```
sudo apt-get install ruby ruby-dev

ruby -v
```

This will install ruby, and ruby dev, allowing us to install compass after this, which is required by Sass

##Install Compass!

```
sudo gem install compass
```

You may be able to run this command without sudo, but I suggest you do as it needs to access your filesytem, but yeah, this will install compass so you can use Sass in your projects!

##Allow npm -g to work without Sudo!

Woah, woah, woah! Wouldn't you want a global install to be able to access your root files and things? And the answer is yes and no. I highly suggest you take the time to do this, npm tends to act weird on anything other than a mac OS, I've used this method and everything works beautifully without any issues. What it will do is keep all of your npm packages in a hidden folder named .npm , so if a package or npm ever starts acting up, simply delete the foler and re-install npm! No more messed up permissions by using sudo with npm all the time!

```
STEPS:

1. go to the following repo: https://github.com/glenpike/npm-g_nosudo

2. Download script, go to its directory and enter the command: ./npm-g-no-sudo.sh

3. For the first question just press enter (leave it blank)

4. For the second one type y , and the press enter (answer is yes)

5. Do what it says and enter the command: source ~/.bashrc

6. ???

7. Profit!!!
```

npm no longer needs sudo, and you can now enjoy a npm error free life :) <3

##Update npm!

```
npm install -g npm
```

It's kind of ironic you can install npm, with npm. But this is how you update npm to it's newest version!

##Install Yeoman (Yo)!

```
npm install --global yo --unsafe-perm
```

Yeoman is an awesome project generator, it does all the hard and heavy lifting of starting a project, and makes it AMAZINGLY easy

#Install some more awesome packages!

```
npm install --global bower grunt-cli ionic
```

--global is the same as -g, bower is another package manager for web development (Yes I know it's weird that you need two, but some packages support one or the other). grunt-cli is the command line interface for grunt, which will host your website on a local server, and will auto-refresh the page as you code it (In other words, the most awesome thing ever, and they have a cool logo), and ionic is an angularJS framework that will allow you to code angularJS and run it through cordova to make your own mobile apps (ionic is optional, but I highly suggest you look into them: http://ionicframework.com/)

#Make sure everything is installed!

```
yo --version && bower --version && grunt --version
```

This will check the versions of everything we just installed in the previous step, make sure they all have versions!

#Install some Yeoman generators!

```
npm install --global generator-angular generator-ionic
```

This will install with npm generators for angularjs and ionic, so you can generate our own web dev projects using yeoman!

##THE END!

Thanks for Reading through my guide! I hope it helped, and feel free to commit or submit any pull requests! Star the repo if you liked it, and don't be afraid to follow me, I'll probably follow back haha! Thanks!

##One Last Side Note!

If you're having any trouble using "ionic serve" or "grunt serve" with ionic see this issue: https://github.com/diegonetto/generator-ionic/issues/209

it will fix everything.

And please remember a lot of the web development frameworks are cutting edge, you may face issues with them that aren't actually you, or your machine, but issues with them. If you're up tot he challenge you should attempt to contribute to them, or create an issue if not leave a reply into one that already exists! Thanks!
