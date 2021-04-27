# Git & CLI Commands

## [Useful Git Commands](https://medium.com/flawless-app-stories/useful-git-commands-for-everyday-use-e1a4de64037d)

| Command | Function |
| - | - |
| `git init` | initialize a local folder as a git repo to be tracked and push to the cloud |
| `git branch feature-1-berger` | Create the branch on your local machine called "feature-1-berger". |
| `git checkout -b feature-1-berger` | Create the branch on your local machine **and** switch into this branch. |
| `git checkout feature-1-berger` | Switch into this branch. |
| `git branch` | return the current branch you are working in. |
| `git status`	| show the status of the working tree |
| `git add <file(s)>	`| add only select file(s) to be staged for commit |
| `git add -A`	| add ALL files to be staged for commit |
| `git commit -m "description of changes"` | commit changes to staged for push |
| `git push`	| push changes to the remote repo |
| `git clone <repoURL>`	| clone a repo into a new directory |
| `git push origin branch_name` | Push the commit to the branch "branch_name" |
| `git pull` | Pulls down changes from the repo to bring your local codebase up-to-date |
| `git push —set-upstream origin resume` |  set the initial push to know where all future pushes need to go in the gitHub cloud. |

## [CLI/Terminal Commands](https://computers.tutsplus.com/tutorials/navigating-the-terminal-a-gentle-introduction--mac-3855)

| Command | Function |
| - | - |
| `pwd` | Print Working Directory, will return the name of the current directory you are in. |
| `ls` | list files in the current directory |
| `cd <directoryname>` | change to a new directory |
| As in | this example |
| `cd workspace` |  will change to a new folder(aka, directory) called "workspace" |
| `cd ..` | move up to the parent folder |
| `mkdir <directoryname>` | make a new directory in the current directory |
| As in | this example |
| `mkdir jsDev` | will make a folder(aka, directory) called "jsDev" |
| `touch <filename>` | create a new file in the current directory |
| As in | this example |
|  `touch index.html` | will create a file inside the current directory called "index.html" |
|  `code .` | open the current directory in VS Code (Macs have to install the PATH) |
|  `echo "USERNAME=meathead" >> .env` | create a file called `.env` and write `"USERNAME=meathead"` inside of it. |
| `mv` | move directory |
| `cp <path-to-file-to-copy> <name-of-new-file>` | copy file |
| `rm` | remove file or directory |
| `tree` | Must install with brew or bash, but is a very useful command to see your entire working directory's tree. |
