# Learning To Program, Like Learning To Cook

It's really not that difficult to learn to program.  It's very similar to learning to cook food.  Allow me to explain.

When you start out with cooking, you follow the recipe exactly as it is, so the meal will taste right.  
If you only ever follow recipes, you will remain a cook (someone who heats up ingredients): you will never become a chef.

However, if you apply yourself, learn the tools and look closely at what the ingredients do in each recipe then you may transform into a chef. 

If you study what you're doing with those recipes, then along the way, you learn incidental things like:

1. How to measure ingredients out properly (using teaspoons, cups, etc.)  
2. How to use spices (what various spices taste like, how strong they are, how they enhance the dish)  
3. How ingredients are mixed properly  
4. Understanding of how ingredients change when heat is applied to them   
5. How various tools (mixers, graters, knives, etc.) work and help you

## Transforming From A Cook Into A Chef

At first, you are just a cook.  You must follow the directions closely and if it is a good recipe you cook up a good meal that people enjoy eating.

### A Cook Must Make Many Recipes

But as you go, if you cook a lot of recipes, you will begin to learn your own way of doing things. Gradually, you will no longer have to strictly follow the recipes.  If you cook enough recipes you'll eventually have no need to look at the recipes.  You'll understand why dishes taste the way they do and you'll understand things you can substitute for ingredients.    
As the old saying goes, first you must learn the rules, then you can break them.  It's true for every great endeavor.

Finally, you'll add your own style to various dishes, adding spices that the recipes have never suggested.  At this point, you will probably begin to have your own custom recipes. That's when you'll transform into a Chef.  And, yet, there will still be things to learn.  There always will be, because cooking food is an unlimited endeavor.

## Beginners Need Great Recipes

For this style of learning to work however, you must do two things:

1. Find great recipes to learn from (learn the basic foundations)  
2. Cook up new challenging recipes as often as possible (do the work)

## A Recipe Is Only The Sum of Its Parts

A very important point is that to learn to cook well, you would never just use the ingredients in isolation from each other.  You would never just mix up spices without applying them to some dish.  You wouldn't do that because the individual parts of the recipe are not the dish.  It is only when all of the parts are put together that you get the edible, delicious dish.

## Learning To Program Is Like Cooking

Learning to program is the same.  To really learn you must bring all the parts together to create an application (a software solution). Unfortunately, the most common way that books, university classes, tutorials, etc. have taught programming: teaching the parts in isolation.  

These sources teach you how to set the value of a variable, write an if statement, a for loop, teach you the syntax of the programming language, etc. but they fail to take you through the steps of building a valuable software solution.

# Unique Learning Proposition

That's my ULP (Unique Learning Proposition) for this book: we will build a complete application which solves an interesting problem.  Along the way we will learn a lot of things.  

Let's take a look at the app we will create and the things you will learn.  Then, after that I'll explain a bit more about why writing a complete software solution is a better way to learn programming.

## Write A Complete App, Learn A Lot of Technologies

Here's a snapshot of the application we'll build as we progress through this book.  
All of the source code from this app is FOSS (Free & Open Source Software) which you can use and change in whatever way that helps you.  

<img width="802" height="629" alt="image1" src="https://github.com/user-attachments/assets/633cf2a4-8d7a-4d21-9e83-84a1dd929c6c" />

**Caption**: Snapshot of DiscoProcs (Discover Processes) running on my Ubuntu 24.04 Linux desktop running KDE Plasma (desktop manager).

## All Source Code Available At GitHub

You can go and look at the source code in the current GitHub repository: [https://github.com/raddevus/DiscoProcs](https://github.com/raddevus/DiscoProcs)

**Note**: I will be rewriting the app as I write this book so the final GitHub repository for this book will include more branches so that you can see the code step-by-step by examining those git branches.  I suspect that the repo from this book will also contain code that is cleaner since I need to explain every line of code in this book.

## What Will The App Do?

The app we will create is a cross-platform TaskManager.

It will allow the user to:

1. **View all processes** which are running on the computer  
2. **View process details,** including  
   1. Process name  
   2. PID (Process ID) ID the OS assigns to the running process  
   3. Path to location where executable is running from  
   4. Exe file date (used as a way to track when the file changes)  
   5. Exe File size (on disk)  
   6. Number of bytes the running process takes in memory  
   7. SHA-256 hash of the exe file (allows us to fingerprint the Exe so we can identify it) – we will learn all about this as we write the code  
3. **Stop any running process**  
4. **Save a Process Snapshot** \- save all processes & related data to a local Sqlite database  
5. **Display a list of all the modules** (program functionality wrapped in code libraries) that the program uses  
6. **Display New Processes** \- Once you take a Process Snapshot, you can then run \[Show New Procs\] functionality and it will examine all the running processes, compare them to the ones that you've stored in the local Sqlite database and determine if they've been captured in the past.  This can give the user an idea of processes that are running that haven't run in the past & provides insight to possible changes to the system.  
7. **Quick Start Any App** \- Add a list of programs you'd like to start then later you can start all of them at once if you like.  Or, you can add parameters to an app that you'd like to start in a particular state and start the app in that state.  
8. **Display all SpecialFolders** \- special folders are locations where the current user can save files and run apps from. These are defined on all platforms (Linux, macOS, Windows) and it can be very helpful to know where they are for discovering where files are located.  
9. **Display Environment Variables** \- Environment variables are Operating Systems values which are used by various running processes. 

# What Will You Learn While Reading the Book & Building The App?

1. The **C\# Programming Language**  
2. **Code reuse** via code libraries (APIs \- Application Programming Interfaces)  
   1. We will start creating our first library function in the next chapter when we start writing code  
3. **Version Control** (we use git and all the source code will be available at GitHub)  
4. **User Interface creation** using "web tools"  
   1. The User Interface for DiscoProcs runs cross-platform but all the major platforms (Linux, macOS, Windows) use different types of window managers and each of those uses proprietary code to display the User Interface. But all those platforms support HTML, JavaScript, CSS  
   2. HTML  
   3. **JavaScript** (including **ReactJS** makes it easier to build HTML components for displaying things like grid views).  
   4. **CSS** (including the **Bootstrap** CSS libraries)  
   5. We will be using a special library named **Photino** (see [Photino.io](http://Photino.io) for more) to build the User Interface using HTML & CSS. Much more on this as we progress through the book.  
5. **ASP.NET MVC WebAPIs** (that's a lot of acronyms)  
   1. **MVC** \- Model View Controller is a way to break up your code to implement SoC (Separation of Concerns)   
   2. **SoC** is the code equivalent of not building a microwave oven that is also a refrigerator.  If your refrigerator breaks down then you have to swap out your microwave too.    
   3. **WebAPIs** are simply functionality that can be called from anywhere via the Internet.  A quick, simple example would be providing the clock time for anyone who calls your WebAPI function.  User sends in a TimeZone ID and receives the current time in that time zone.    
6. **SQL via Sqlite**  
   1. We will store data in a Sqlite database.  
   2. DDL Data Definition Language (create database tables)  
   3. SQL (Structured Query Language) (query the database \- get and store data)  
   4. EF Core (EntityFramework core)  
7. **File & Folder details**  
   1. Learn to get the list of SpecialFolders (folders where user data is commonly stored on various Operating Systems)  
   2. Learn to read data from files & write data to them.  
8. **Operating System Concepts** \- As you learn to program this app there are numerous OS concepts you'll learn along the way (Processes, Files, Folders, environment variables and more)

This is not a complete list of everything we will cover.  Just as it is with cooking, there are a lot of incidentals that we will learn along the way.  For example, if you haven't installed .NET Core SDK (Software Development Kit) on your computer yet, there are numerous things you'll learn as you do that work.

# How Writing A Complete App Enhances Learning

## Human Memory Is Contextual

The research on memory shows that memorizing a list of things is very difficult for humans.  
The average person can remember somewhere between three and seven items.  
Memorizing a long list of random items is similar to learning a bunch of interesting facts and code snippets in a programming language, but never applying them.  They're very difficult to remember.

However, there are humans who can memorize huge lists.  How is it possible?  Researchers have discovered that these people create context around what they are memorizing.  Context means story.  So if a person creates a story around what they are trying to remember the brain is engaged and remembers things.

## The App We Build Will Be Like A Story

To learn to develop software this book will guide you step-by-step through creating a cross-platform application (runs on Linux, macOS and Windows).  The work we put into creating the application will create a "story context" for the esoteric programming language details that you learn.  That context will help you remember what you've learned.  It's way more fun than reading about how to write a for loop and you'll have a complete application when we're done. 

Since the code is FOSS (Free and Open Source Software) you can alter the app for your own use, use code from the project in your own apps that you write in the future and use the code however you want.

## Create A Complete Usable Software Solution

Creating a complete application is a big challenge to take on, but I will be with you along the way and you will see that there is nothing extremely difficult about learning to program.  You don't have to be a genius to do it.  

### Not Everything Will Be Easy

Of course, not everything will be easy.  There will be some hard things to do that may trip you up.  But, I'll do my best to help you know which things may cause you some grief.  That's what I'm here for: to point out the things that may be difficult and guide you through.

### Not False Humility: I'm Not The Smartest Person

I'm really not that smart. I'm average, like most people.  I don't have a college degree but I've been employed in the IT Industry with no breaks (never been fired yet 😁) for 35 years.  I've been developing software professionally since 1999\.  I've used a long list of programming languages and technologies to write that software, and I've discovered that you don't have to be the smartest person in the room to do some cool things.

Secret: The smartest person in the room often goes down the wrong road because they're convinced they're right.

If you don't have to be the smartest person, then what skills do you need?

1. **Curiosity** \- Desire to learn.  Ask a lot of questions (even when you think you know the answer).  
2. **Tenacity** \- Be relentless

If you are curious then you'll try to understand.  
If you're tenacious then when a technology fails to do what it is supposed to do, you'll look for an alternate way of getting to the solution and you'll keep fighting building the solution.
