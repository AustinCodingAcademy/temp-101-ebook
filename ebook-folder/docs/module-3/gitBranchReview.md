# Git Branch Review

*“There is in every true woman’s heart a spark of heavenly fire, which lies dormant in the broad daylight of prosperity; but which kindles up, and beams and blazes in the dark hour of adversity. “ –Washington Irving*

## Overview
<!-- ! Video Contents: 101 - Git Branching  (width="655" height="368", ratio 1.77) -->
<iframe src="https://player.vimeo.com/video/407583549" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

So far we've used the git software for it bare minimum capabilities: `add` files, `commit` them to the staging area, check the `status` of our changed files, and `push` the changes to a remote repository. This is great, btw! Mastering these commands is crucial to your success because you'll be using them everyday of your development career. However there are three command we need to introduce now so you can further grow as a developer. They are: `git branch`, `git checkout`, and `git pull`.

## Branching

Throughout each of your projects you've been working on your own in a single branch: `master`/`main`. And this is fine if you're working by yourself because you don't have other developers changing the code causing **merge conflicts**. But, next week you'll begin collaboratively working with classmates on projects to prepare you for working on teams in your career. Remember, websites are not built by a single person, they have many teams, each with multiple people working on specific aspects of the website.

In order for these teams to work together and not mess each other up as they do it, they use a functionality of git called **branching**. Branching means that we create an identical copy of the current code base onto a virtual branch that is connected to the main branch.

Let's say you and your nearest classmate began working on a project, you or they could create a repo that includes a `README.md` file and an `index.html` file. Then you both clone it to your local computers. If you open it up it will be on the `master`/`main` branch and so will theirs.

If you both code on this same branch then try to `push` the code up, it won't allow you to because there will be a conflict in the files.

To safely, prevent against this you could create a branch **off of** `master`/`main` called something like: `jills_landing-page-branch` and your partner could create another branch **off of** master called: `jacks_gallery-page-branch`. Then you both could code up what you need to do. When you're finished, git push to add the code to the repo, but on a different branch than master or `jacks_gallery-page-branch`. Before you two *merge* these branches into `master`/`main` you would review Jack's code and Jack would review your code.

The point of branching & reviewing is that each of the developers on a team get to work with the same code base but not introduce bugs as easily.

  >  Note: As of the writing of this ebook, gitHub is in the process of switching the name of `master` branch to `main` branch.
  > Henceforth, we shall call `master` as `main`.

### How to Branch

It's actually just as easy as any of the other git commands. Once you've cloned a repo you can:

1. create a new branch: `git branch jills_landing-page-branch`
1. switch to that new branch: `git checkout jills_landing-page-branch`
1. *or* do **both** at the same time: `git checkout -b jills_landing-page-branch`

Look at those three commands one more time. One creates a new branch, another changes your workspace to the branch, and the other does both at the same time.

  > NOTE: If you've created a new branch you can't create the same branch again. You'll just use `git checkout` to switch between it and `main`, `git checkout master`

  > MAJOR NOTE: When you read **off of** `main` above, this means that you should only create a branch while in `main`, **not off** of another branch. If you do that, you'll create a branch off of `main`, then another branch off of that new branch and so forth and so forth. This is not good and you'll loose track of where your code is. DO YOURSELF A FAVOR, **only** create a new branch if you're currently on `main`.

What you should have learned:

- [ ] Why we need branches.
- [ ] When to branch.
- [ ] The difference between each of these commands:
    * [ ] `git branch branch-name`
    * [ ] `git checkout branch-name`
    * [ ] `git checkout -b branch-name`
- [ ] Only branch **off of** `main`

## Merging & Pulling

Merging usually only happens in GitHub not on the terminal. After you `push` up the changes from your personal branch to the repo, you can go to the repo on GitHub and create a **Pull Request**(PR). This is your request for the code base administrator, i.e. your partner or team lead, to *pull* your code into the `main` branch.

If they review your code and determine that it is clean, bug free, and accomplishes the tasks it is suppose to do then they will **merge** it into `main` and normally delete your personal branch from the repo.

Then you will go to your terminal and find the code base your team is working on and switch to the `main` branch (`git checkout main`) so you're back in the main code base. Since your team lead has merged your latest changes to `main` you can run the command `git pull` to pull all of the code that was merged to `main` since you cloned it. These merged changes would include your code and all of your teammates' code as well.

The process would continue from there when you received your next task where you would create a new branch off of `main`, make your changes, `git push`, create a **PR**, wait for the merge to be approved, then `checkout main`, and `git pull` the changes again. *Repeat, over and over again for the rest of your career.*

What you should have learned:

- [ ] We create new branches to have a personal sandbox for us to build our code.
- [ ] When we're finished we `push` those changes and create a **Pull Request**.
- [ ] Then our team lead approves and merges that branch into `main`
- [ ] After that, we `checkout` back to `main` and `git pull` all the latest changes.
- [ ] Then we start over again by `git checkout -b new-branch-name`.

### One Small Gotcha

After you've created your new branch, the remote repo won't know about it because it currently only exist on your **local machine**. This means that when you attempt to `git push` you'll get an error that looks something like this:

```console
➜  101-git-practice git:(jills_landing-page-branch) git push
fatal: The current branch jills_landing-page-branch has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin jills_landing-page-branch
```

Yes, the `fatal`: sounds terrifying but all it really means is that the command you last put in didn't resolve/complete. And, git is so nice that it gives you the fix with the error message!!! Do you see the line that starts: `git push --set-upstream`....? Just copy/paste that line back into the terminal = ++enter++ and it will resolve the issue.

  > STUDENT: 'What does that line do?'
  > INSTRUCTOR: 'It creates an origin in the repo that matches what's on the local computer.'
  > STUDENT: 'So, it creates a branch on the remote repo that's called: `"jills_landing-page-branch"`?'
  >INSTRUCTOR: 'Yes. Using the additional arguments: `--set-upstream` and `origin` we can tell the `push` function to create a place for this code to go that is on the original repo as well as push the new code up! Look at the docs for `push` for more information.

## Additional Resources

- [ ] [YT, Jake Vanderplas - Creating a Simple PR](https://youtu.be/rgbCcBNZcdQ)
- [ ] [YT, helpmecoder - Git Branching & Merging](https://youtu.be/hufGg2mf7eA)

## Know Your Docs

- [ ] [git SCM Docs - branch](https://git-scm.com/docs/git-branch)
- [ ] [git SCM Docs - checkout](https://git-scm.com/docs/git-checkout)
- [ ] [git SCM Docs - pull](https://git-scm.com/docs/git-pull)
- [ ] [git SCM Docs - push](https://git-scm.com/docs/git-push)

  > [What's SCM mean](https://www.google.com/search?q=what+does+scm+mean+in+git+scm)?

<!-- ! END OF VIDEO 101.1.3.1 - TITLE-->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

<!-- 

```javascript

```

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | Fetch resource                       |
| `PUT`       | Update resource |
| `DELETE`    | Delete resource |


    `line numbers`
:do you like 'em?


++slash++
https://facelessuser.github.io/pymdown-extensions/extensions/keys/

=== "Javascript"

    ```javascript
    ```

=== "Python"

  ```python
  ```

=== "Example"
    ```console
      .
    ```

=== "Instructions"
    ```markdown
      .
    ```

=== "Result"
    ![PIC](./../images/pic.png)
-->