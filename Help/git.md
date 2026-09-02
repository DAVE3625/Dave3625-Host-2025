# Mini Git Helper

*Super short, non-formal guide for working with Git and GitHub. GitHub has a bunch of good guides that elaborate way better. LLMs can be helpful for troubleshooting!*

*If you see commands in this guide, like "now you can run `git status`", this means to run it in the terminal. Make sure you are in the right folder!*

## TL;DR
If you don't want to know why, but you just want it to work. 
* Download [Git](https://git-scm.com/downloads)
* Clone the repo by going [here](https://github.com/DAVE3625/Dave3625-Host-2025/tree/main#), click the big green **code**-button, copy the link, and run `git clone linkkyoujustcopied`. 
* * You don't need to make new branches 
* Run `git pull` every now and then to get the latest changes 


---

## What is a repo?

* A project folder tracked by Git. Our repo is called Dave3625-Host-2025.
* It has files + history + branches.

## Short summary of Git, GitHub, and all this repo stuff

#### Git

Git is a version handling tool you install on your PC. Every time you update your code, you can add a "save point" called a commit. This stores the code state and lets you easily manage the project history.
[How to download Git](https://git-scm.com/downloads)

#### GitHub

GitHub is a platform that lets you store git history. Imagine Git and GitHub like YouTube. Commits and projects are like videos, and YouTube is where they are hosted.

#### Branches

People use **branches** to work on new things without breaking the main code, and more people can also work in parallel. When you make a new branch, it copies all the code from the commit you branch out from.

The main branch is called `main` (crazy!). In big projects, you'll normally have loads of branches for making new features, some testing branches, and other long-lived branches for releases. Check which branch you are in in VS Code in the lower left corner. To see what changes you have made, you can either run `git status` or click the source control menu on the left side. 

You have a version of all branches on your PC (local) that you have looked at (checked out, `git checkout -b branchname`), and there's what's hosted online (remote). You have to pull changes from remote into local branches to make sure you are up to date. ```git pull``` gets the changes in the branch you are currently in. 

Specify that you want to pull or push changes to a remote branch by specifying `origin/branchname`, like `git pull origin/branchname`. If you ever push to a repo and it doesn't show up in GitHub, check that you pushed to the remote branch. 

When a branch is ready (code is good to go), it gets merged back into `main` (or whatever the mainline branch is). This keeps the history clean and the main code stable while letting people experiment elsewhere.
[How to make a new branch](#how-to-make-a-new-branch)

You can all pull from this repo. You cannot push because you don’t have access. Read more about how to store your own code under ["Saving your own changes"](#so-how-do-i-save-my-own-changes).


## Cloning a repo

1. Copy the repo URL from GitHub/GitLab.
2. Run one of these:

   ```bash
   # HTTPS (asks for login/token on push)
   git clone https://github.com/DAVE3625/Dave3625-Host-2025.git

   # SSH (needs setup, but no passwords later)
   git clone git@github.com:DAVE3625/Dave3625-Host-2025.git
   ```
3. Move into it:

   ```bash
   cd Dave3625-Host-2025
   ```

### HTTPS vs SSH

You don’t need to use SSH just for pulling changes, but I recommend you set it up anyways!

The differences are:

* **HTTPS** is quick, works everywhere, but asks for login often.
* **SSH** needs a one-time setup (tedious if you’ve never done it), but then you can push changes without logging in every time.


## "So how do I save my own changes?"

In this class, just keep them locally on the `main` branch. Example: clone the repo, make changes in labs as you need, and run `git pull` every now and then to get updates.

Here are other ways to manage your own changes. They may be useful for other projects.

### Forking (when you don’t have write access)

1. On GitHub: click **Fork** -> creates your copy.
2. Clone **your fork**:

   ```bash
   git clone git@github.com:YOURUSER/Dave3625-Host-2025.git
   ```
3. Add the original repo for updates:

   ```bash
   git remote add upstream https://github.com/DAVE3625/Dave3625-Host-2025.git
   ```
4. Make a branch, commit, push:

   ```bash
   git checkout -b feature/thing
   git add <files>
   git commit -m "short message"
   git push -u origin feature/thing
   ```
5. Open a Pull Request from your fork -> original repo.

### Branches

In this course, since you don’t have write access, you won’t be pushing anything to the repo. You can make your own branch locally, and all your code will be saved just on your PC. But just be aware that this branch will not get all our changes automatically — you need to be on `main` for that.

#### How to make a new branch

1. Clone the repo normally.
2. Make a branch:

   ```bash
   git checkout -b branchname
   ```
3. Commit (local only in this course):

   ```bash
   git add <files>
   git commit -m "short message where you describe what you did, like 'made new branch'"
   ```
4. (Optional) Push to a repo you control (like your fork). Otherwise it just stays local. Remember that you can't push to main.

   ```bash
   git push -u origin branchname
   ```
5. If you push somewhere you have access, that’s when you’d open a Pull Request.



## Setting up SSH keys

SSH keys are a secure way to log in to GitHub without writing your password all the time. One-time setup and you’re done.

1. Generate a key:

   ```bash
   ssh-keygen -t ed25519 -C "username@oslomet.edu"
   ```

   * Hit Enter for defaults.
   * Add a passphrase (optional and recommended).

2. Add it to the SSH agent:

   ```bash
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_ed25519
   ```

3. Copy the public key:

   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```

   Paste this into GitHub: go to **Settings -> SSH Keys -> New SSH key**.

4. Test it:

   ```bash
   ssh -T git@github.com
   ```

   You should see a success message if it’s working.



