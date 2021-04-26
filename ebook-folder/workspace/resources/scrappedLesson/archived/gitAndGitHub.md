# Managing Versions of Code with Git & GitHub

Remember, in a Flipped Classroom you will study and consume your "lecture" *before* you come to class, so that you can take advantage of your time in class to practice and apply concepts with the guidance of your instructor and support of your classmates. With the guidance of your instructor you will be able to confidently make mistakes, run into errors, and find bugs in your code. But for all of this to happen, you must make sure that you complete your pre-homework before each class.

Let's begin:

On the first day of class we will hosting your the portfolio webpage that you built in the previous lessons. To do this, you will need the Git software to move the files from your local machine (*computer*) to a remote repository on GitHub from where it will be hosted live on the internet for anyone that has the URL to see!

## Checklist

- [ ] Overview of Git & GitHub
- [ ] Create [GitHub Account](https://github.com)
- [ ] Download & Install [Git Software](https://git-scm.com/)
    * [ ] *for Mac* Download Git + xCode  
    * [ ] For *for Windows* download gitBash
    * [ ] Set git configurations and navigate VIM
- [ ] Learn more about Git

## Overview - Version Control with GitHub

<!-- ! Video Content: Clayton@ACA - 101 - Version control:  -->
<iframe src="https://player.vimeo.com/video/388133919" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
  
*****

### Read It - Git Software

With all software, including the desktop and mobile apps that you use every day, developers are always making changes and updates. Think of all the times you've been asked to update to the latest version of an app on your phone. The reason the company asks you to do this is because the team of developers have fixed bugs, improved efficiency, or add/removed features. These changes are happening all the time, all day long across an entire team of developers but are only released every so often to users. To manage all of these changes, a system called **version control** was developed. Of all the version control softwares available, **Git** is by far the most popular – and it's free!

As you read above, using a version control software like Git is incredibly important as a developer. Version control allows for multiple developers to work on the same codebase at the same time, revert selected files back to a previous state, revert an entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. This helps developers work more efficiently, effectively, and responsibly when editing code.

### Read It - GitHub

**GitHub** is a web application that works with *git*. It is a place we can store code to share with others and collaborate on projects simultaneously or asynchronously. In class and in your job, you will use GitHub every day to:

* store your code online (in the *cloud*)
* host and share your projects in this class
* share your code's Pull Requests (PRs) with your instructor or team
* receive comments on your code from your instructor or team

We're going to start by creating an online account on [GitHub.com](https://github.com/). After setting up your account we will walk through the steps of downloading the git software and learning a few of its __many__ commands. Before getting started, be aware that Git works in what is called the "Command-Line Interface". You probably won't feel comfortable with this interface __yet__ but you soon will be. I promise!

### See It - How Git Works

<!-- ! Video Content: YT, Paul Programming - What is git? -->
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/OqmSzXDrJBk?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Create a GitHub Account

1. Go to [GitHub](https://github.com/) and create an account.
1. **Be sure to use a professional name like `firstNameLastName` for your username** It will be the first thing on your resume for potential employers to read!!!!!!
1. **IMPORTANT** Write down your username and password...**We will be using it again soon.**

<!-- <iframe src="https://player.vimeo.com/video/292779452" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe> -->

<!-- 101 - What and How - GitHub:  -->
<iframe src="https://player.vimeo.com/video/389352161" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

*****
*****

Download [Git Software](https://git-scm.com/)

### Download Git Software

To use the software Git, we will need to get comfortable using the Command-Line Interface (aka CLI or "terminal"). Depending on your Operating Systems (OS) you will need to follow different instructions to access your terminal and download Git:

=== "For Window <10"

    <iframe width="560" height="315" src="https://www.youtube.com/embed/J_Clau1bYco" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    
    - [ ] Install [Git](https://git-scm.com/download/windows)
    - [ ] Additional support: [Blog, GitHub - Install git](https://git-for-windows.github.io/)
    - [ ] See **For All Machine Users** below for next steps.

=== "For Windows >10"

    - [ ] If you have a Windows 10+ machine you can use [Command Prompt](https://www.howtogeek.com/235101/10-ways-to-open-the-command-prompt-in-windows-10/)
    - [ ] [YT, Programming Knowledge2 - How To Install Git on Windows](https://www.youtube.com/embed/J_Clau1bYco)
    - [ ] Install [Git](https://git-scm.com/download/windows)
    - [ ] Additional support: [Install git](https://git-for-windows.github.io/)
    - [ ] See **For All Machine Users** below for next steps.

=== "For Mac"

    <iframe src="https://player.vimeo.com/video/292802914" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

    - [ ] Go to terminal ++cmd+space++ then type `terminal` + ++enter++
    - [ ] Install [HomeBrew](https://brew.sh/) - in the terminal run: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` + ++enter++
    - [ ] Fix packages - in the terminal run: `brew doctor` + ++enter++
    - [ ] Install [Git](https://git-scm.com/download/mac) - in the terminal run: `brew install git` + ++enter++
    - [ ] You may be prompted to type in a password. This is your computer's password and will not appear as you type it for security reasons.
    - [ ] You will be offered to install the Command Line Developer Tools (Xcode) from Apple. Confirm by clicking Install. After the installation finishes, continue installing Homebrew by hitting **ENTER** again. Xcode is required by Apple and may take a while to install. *Please do this before class.*
    - [ ] See **For All Machine Users** below for next steps.

=== "For Linux"
    - [ ] Use your package manager to install the latest version of Git: `sudo apt-get install git`
    - [ ] See **For All Machine Users** below for next steps.

  > NOTE: There is no icon for this program, just go to your terminal/shell/commandPrompt/bash and type git + ++enter++

### Git Config for All Machine Users

 **Set your Git username and email.**

You must configure your local Git software to know where to push your work to. We do this by telling it our GitHub username and email address. We also have to provide it with our GitHub password. Follow these steps.

> NOTE: **if you see a strange looking screen pop up, it might be VIM.** *See the instructions below to find out how to navigate VIM.*

1. In the your terminal copy/paste this code and replace YOUR USERNAME and EMAIL with the info you used to create your GitHub account above:
    `git config --global user.name "YOUR USERNAME"`

    then ++enter++

    `git config --global user.email "YOURemail@address.com"`

    *If it asks you for a password this is your GitHub account password*

> NOTE: !! make sure you REMOVE the `#` at the beginning of the lines where you paste this configurations in. Lines beginning with `#` are read as a comment in configuration files like this `.gitconfig` file and won't be read by the git software.

*****

#### *Possible* Step 4. VIM / VI

When doing your `git config` you may see a more unusual window in your terminal. It will have a bunch of `~` or `#` along the left side. This is a built in text editor like VS Code but very stripped down. It allows you to change files and write code. For this step you'll be changing your git config file to contain your username, email.

VIM has two modes *insert* (input text) and *command* (move around and do stuff). For now, we really only need *insert* but you'll need to know how to get in and out of the two different modes.

Type ++i++ to enter *insert* mode and type ++esc++ to enter *command* mode. You'll know which one you're in because "insert" will appear at the bottom of the screen when you enter *insert* mode.

For now, navigate around the page with your arrow keys (d-pad). When you need to type in your email or something type ++i++. You're then free to type in whatever you need.

When you're finished, type `esc` to move back to *command* mode. To exit and save the file type `:wq` + ++enter++ (write and quit). This simply says to the computer, "I'm about to give you a command, write the file, then quit the program."

If you're lost, it's totally fine. VIM is an old relic that's stuck around and become a hipster text editor but really it's there so you can always change files, no matter what!

### See It - gitconfig & Vim

<!-- ! Video Content: Clayton@ACA - gitconfig and Vim -->
<iframe src="https://player.vimeo.com/video/384020788" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

*****
*****

## The First Terms to Know in Git

* **GitHub** is a place you can store, demonstrate and collaborate with other developers on your codebase. You can hold your own code there (which is what we'll be doing in the next class) as well as copy other people's code and build off of it in your own personal projects!

* **Git** is a *version control* and source code management system that developers use to manage and store their code.

    * Git allows a code base to be updated by multiple people in a safe manner that will not affect the end users' experience.
    * Git gives us a way to develop and fix code in development "branches" and then merge it into a stable and safe branch.
    * Git is how real world development occurs. It is also how you will turn in assignments. In this way you will become very familiar with the tools you'll use in your profession.

* **Version Control** is the process of iteration from one version of software (code) to the next version of software. With each minor improvement of the software bugs may be inadvertently introduced. Using version control, developers can retroactively find when and where the bugs were introduced and more quickly remove them!

* A **branch** is a copy of the whole codebase. It acts as a code sandbox for you to work in safely without change the whole codebase. In each branch, you can work on small fixes and improvements, test them, and prove their efficacy without bugs before you *merge* the changes or the branch, back into the whole codebase.

## Additional Resources

Git is usually a hard concept for new programmers to wrap their minds around. Don't worry, you will get Git by the end of this course – if not by the end of this week. But to make sure you understand it sooner, watch these videos and write down all of your questions, thoughts and epiphanies to bring into class for healthy discussion and discovery!

* [YT, The Coding Train - What are Git and GitHub?](https://www.youtube.com/embed/BCQHnlnPusY)
* [YT, Traversy Media - Git Crash Course](https://www.youtube.com/embed/SWYqp7iY_Tc)
* [YT, Code Insights - Git in 20 Minutes](https://www.youtube.com/embed/Y9XZQO1n_7c)
