---
layout: guide
category: guide
title: How To Become a Web Developer - Unfinished
shortDescription: An unfinished guide on how I learned how to become a web developer.
---
## Compilation of Tools/Guides to learning how to develop websites and apps!

This Guide will ask you to complete several Lessons from [Code Academy](https://www.codecademy.com/). And it will ask you to install a lot of programs onto your machine. **IF YOU RUN INTO ANY PROBLEMS AT ALL, GOOGLE IS YOUR FRIEND, PLEASE GOOGLE AND TRY TO FIND THE ANSWER, IT IS A LIFE LESSON THAT YOU WILL RUN INTO AT SOME POINT IN THIS GUIDE.**

**INDEX**

1. [Part 1: Installing A Development Environment](https://github.com/torch2424/How-To-Become-A-Web-Developer#part-1-installing-a-development-environment)
2. [Part 2: CodeAcademy Lessons](https://github.com/torch2424/How-To-Become-A-Web-Developer#part-2-codeacademy-lessons)
3. [Part 3: Your First Website!](https://github.com/torch2424/How-To-Become-A-Web-Developer#part-3-your-first-website)

## Part 1: Installing A Development Environment

So, in this guide we will be using Linux (Specifically Ubuntu). Which will already bring a lot of questions. Why Not Windows? Because Windows is terrible and extremely difficult to do any web development, windows is only really useful in programming in Unity or other windows apps. Why Not Arch (Or any other Linux)? Every Linux OS has its pros and cons, I noticed that Ubuntu tends to have good support, and allows you to take full control of your computer with Linux tools and things, but don't make you frustratingly install everything from source, and spend hours trying to do simple tasks. However, if you don't mind this, and want to have even more power than ubuntu, searching for an other Linux OS for your development might prove useful for you. Why not Mac OSX? I will admit, for web and app development, OSX IS KING. There, I said it, I hate to admit it, but it’s true. Partly because apple doesnt let you develop for it’s devices without developing on an apple machine, and also, a lot of web developers tend to use macs, because they get things done. They dont always get it done the best, but they get it done. However, I am a PC user, and I am guessing you are too, so we are going to install Linux (Specifically Ubuntu), which also happens to be the most “beginner friendly” so it shall help with learning the ropes.

Now, you have two options, you can try [Ubuntu](http://www.ubuntu.com/) or [Elementary OS](https://elementary.io/). Elementary OS is simply a prettier and faster derivative of Ubuntu, which I choose to develop in and very much enjoy and very much recommend. Both are a good choice. But once you choose, please follow these guides (One of them or bits and peices from all of them) to get it installed (You are going to need a usb flash drive to get it on there, and these guides will overlapp one another):

1. [HowToUbuntu](http://howtoubuntu.org/how-to-install-ubuntu-14-04-trusty-tahr)
2. [Wikihow](http://www.wikihow.com/Install-Ubuntu-Linux)
3. [PsychoCats](http://psychocats.net/ubuntu/usb)

There is another option, which would be to install virtual machines using [Vagrant](https://www.vagrantup.com/), but since we are starting out, I suggest you install the OS so your more comfortable with the enviornment, before we virtualize it.

Please be careful, you can wipe your hard drive from doing this, so if you can backup all of your files on windows. And please read the instructions at the bottom about booting from a usb device, because once you boot from usb, it will be pretty self explanatory. If something looks weird or doesn't make sense (Such as partitioning please google things like “Ubuntu/Elementary Install Partitioning with Windows 7”. I am hoping you will learn to google your way out of problems)

Once Ubuntu is installed, You're going to need some fancy/fun software to get you using the OS, and get you developing later on. I actually wrote up some of my own guides on github that you should follow, and will get your OS running and Looking great!

1. [Part 1, OS apps and packages](https://github.com/torch2424/Elementary-Ubuntu-Initial-Dev-Install)
2. [Part 2, Web development tools and package managers](https://github.com/torch2424/Elementary-Ubuntu-Web-Dev-Environment)

Please try your best to use the Operating system as much as you can for things like browsing the web, downloading/playing music, etc...The more comfortable you are with your development environment the better. Plus this will help you learn how to use Linux/Unix which is what Most developers use, and will help you become a better developer. Specifically, try to play around with the terminal, it makes you look cool, and its where the real magic hapens in Linux

This should conclude creating your development environment. Please note, that Part 2 of the Elementary-Ubuntu Guides I wrote will be referenced later on, please make sure these are all installed correctly, as they will be required once we start our first project.


## Part 2: CodeAcademy Lessons

Next, we’re going to start learning how to code with some simple Code Academy lessons. The suggested last unit will be in parantheses like so: (Unit 1)

P.S These won’t teach you how to make a product, but simply the basics and syntax of code to get you started.

For these lessons, please keep in mind they do not need to be completely finished, if you do about Most (if not half) of the lesson, And you can probably skip most of the review projects/quizes, and you should be good to go (You can learn the rest while developing)!

1. [Linux Terminal Command Line (Unit 1)](https://www.codecademy.com/learn/learn-the-command-line)
2. [Html And Css (Unit 6)](https://www.codecademy.com/learn/web)
3. [Javascript (Unit 6)](https://www.codecademy.com/learn/javascript)
4. [AngularJS (Unit 1) (May want to skip if you want to go straight to Angular 2, but having an understanding of Angular 1 would help significantly in learning any javascript framework and the Next Part will feature making our own project in Angular 1, as it is still a great framework to know and has plenty of jobs, and is alot of fun)](https://www.codecademy.com/learn/learn-angularjs)

## Part 3: Your First Website!

A good starting point for your first website, is going to be a website for yourself! Your personal website/portfolio is going to be your one stop shop for anyone who wants to see your code, your projects, and who you are. And it should ALWAYS be your best project. For example, you make a new app or website that uses some cool new design skills, animation, cool functionality etc…It should be implemented in your own website ASAP after that app is released. From what we learned above, we should be able to look something like [my personal site](http://aaronthedev.com/#/). Now that we have the development environment, and the basics of coding, we are going to generate a project, and get developing on it!

In Part 2 of the Elementary-Ubuntu Guides, We installed Yeoman (yo). So first things first we want to do is generate a project. So, open a terminal, cd (Change directory) into a folder you want the project to be generated into, and type “yo”. In this menu, choose generator-angular. And then it will ask you some questions. Say No to gulp (Grunt FTW), say yes to sass (Even more powerful CSS), say yes to bootstrap (this will make jquery a dependency, and is soething you want to never use in angular, but since we’re starting out and it is required for the yeoman default theme, we will let it slide, but I highly suggest not using any jquery in your own code), and simply press enter for the plugins. And the project should be generated! (Please make an educated guess (Google for the answer) if any other questions appear).

So, now that we have our project, we need to install its dependencies (Other packages and plugins we are using to make the project). So first type “npm install”. Then after that completes, type “bower install”. Finally, type “grunt serve”, some text will fly up, and a new browser tab or window should show with or website! Cool huh? And the even cooler part is that Grunt uses something called “livereload” that will reload this web page whenever we make a change to the files! So let’s do that!

Open up the project folder in your text editor of choice, I use and suggest [Atom](https://atom.io/) and you can begin editing your files! Note you have things such as package.json, gruntfile.js, and bower.json. And these all manage what the title implies, things like the packages, grunt, etc… but they are quite complicated and can be learned later in another project or something. But for now, to make changes, our HTML is in app/views, our Javascript is in app/scripts, and lastly, our CSS (or Sass) is in app/styles. Please note that [Sass](http://sass-lang.com/guide) has to compile before showing changes on the website, grunt will do this automatically, but it takes like 5 seconds every large change you make.

Please try and make this website your own. If you need any additional pages or controllers, etc.. please look at the [Github repo for the Yeoman Angular Generator](https://github.com/yeoman/generator-angular). Try doing this such as changing the site colors, adding more pages, changing images, adding animations, making a list ng-for, etc… If you get stuck PLEASE GOOGLE AND TRY YOUR BEST TO FIND YOUR ANSWER. Also, here is the [source code/github repo for my personal site](https://github.com/torch2424/PersonalSite) if you would like to see anything I did you would like to try.

## TO BE CONTINUED

Things still to be covered, wrap up the personal site, Part 4: Building and hosting (Need to write up a guide to digital ocean first), Part 5 Github https://www.codecademy.com/learn/learn-git http://rogerdudler.github.io/git-guide/ <-- the no deep guide , Part 6: Ionic, Part 7: Expanding your knowledge, Having Fun, and becoming a professional
