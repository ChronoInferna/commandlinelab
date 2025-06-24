# Lab: Getting Comfortable with the Command Line

## Overview

In this lab, you will explore the basics of the command-line interface (CLI).
You'll learn how to navigate directories/folders, create and manage files, and run simple commands.
By the end of this lab, you’ll have created a basic personal directory structure and written your first helpful shortcut.

---

## Goals

- Understand what the command line is and how to use it.
- Navigate the file system using CLI commands.
- Create, delete, and organize files and directories.
- Use basic shell commands (`ls`, `cd`, `touch`, `mkdir`, `rm`, `cp`, `mv`, `cat`, etc.).
- Create simple aliases to speed up your workflow.

---

## Part 0: Introduction to the Command Line

The command line is a text-based interface that allows you to interact with your computer's operating system.
It is a powerful tool for performing tasks quickly and efficiently, especially for developers and system administrators.
Many tasks that can be done through a graphical user interface (GUI) can also be accomplished through the command line, often with greater speed and flexibility.
Commands are usually typed into a terminal or console window, and they can include options (flags) and arguments that modify their behavior.

TLDR: Use the terminal if you want to be FAST.

---

## Part 1: Command-Line Scavenger Hunt

Use the terminal to complete the following steps. You may write down the commands you use as notes.

If you're using Windows, you can open the Command Prompt by searching for "cmd" or "Command Prompt" in the Start menu.
If you're using Mac, you can open the terminal by searching for "Terminal" in Spotlight (Cmd + Space).
If you're using Linux, you probably already know how to open your terminal. If you don't, a quick Google Search for "how to open terminal on [your Linux distro]" should help.

1. Print your current directory:

   ```bash
   pwd
   ```

   This will probably return something like `/home/your_username` on Linux or Mac, or `C:\Users\your_username` on Windows.

2. List all files and directories in your current directory:

   ```bash
   ls
   ```

   > [!NOTE]
   > You can pass in "flags", usually marked with a dash, e.g. `ls -l` for detailed information or `ls -a` to include hidden files. You can also combine flags, e.g. `ls -la` to show all files in detail.

3. Change to your home directory:

   ```bash
   cd ~
   ```

   > [!IMPORTANT]
   > The `~` symbol represents your home directory. You can also use `cd` without any arguments to go to your home directory.

4. Create a new directory called `my_lab`:

   ```bash
    mkdir cli_lab
   ```

   > [!NOTE]
   > Feel free to to make whatever directory structure you want, especially if you want to store all your other school stuff here. It is your computer after all! For the sake of this lab, we will assume you are creating a directory called `cli_lab` in your home directory.

5. Change into the `cli_lab` directory:

   ```bash
   cd cli_lab
   ```

6. Create three new directories inside `cli_lab`: `projects`, `notes`, and `scripts`:

   ```bash
   mkdir projects notes scripts
   ```

7. Create a new file called `README.md` in the `cli_lab` directory:

   ```bash
   touch README.md
   ```

   > [!NOTE]
   > The `touch` command creates an empty file if it doesn't exist, or updates the timestamp of the file if it does.

8. Create a file called `README.txt` that says “Welcome to my command line workspace!”:

   ```bash
   echo "Welcome to my command line workspace!" > README.txt
   ```

   This takes advantage of the `echo` command, which prints text to the terminal, and the `>` operator, which redirects that output to a file.

   > [!NOTE]
   > You can try creating the file with `touch README.txt` first, then using a text editor like `nano` or `vim` to edit it.

9. View the contents of `README.txt`:

   ```bash
   cat README.txt
   ```

   The `cat` command displays the contents of a file in the terminal.

10. Copy `README.txt` to `notes/README_copy.txt`:

    ```bash
    cp README.txt notes/README_copy.txt
    ```

    The `cp` command copies files or directories.

---

## Part 3: Going Beyond the Basics

As you can see with all the notes, there are many ways to do the same thing in the command line.
We hope that you have not been buried in all this new information, but this is especially important to learn as it is the language you need to effectively navigate your own computer.
Here are some additional commands and concepts that will help you become more comfortable with the command line:

1. `vim`: A powerful text editor that runs in the terminal. It has a steep learning curve but is very efficient once mastered.
   - To open a file: `vim filename`
   - To enter insert mode (to edit text): Press `i`
   - To return to command mode: Press `Esc`
   - To exit without saving: `:q!`
   - To save and exit: `:wq`
   - `vim` has as ton of features and shortcuts which are worth learning. You can find many tutorials online, such as [Vim Adventures](https://vim-adventures.com/) or [Open Vim](https://www.openvim.com/). Some computers may even have `vimtutor` installed, which is a built-in tutorial on the command line.
2. `git`: A version control system that allows you to track changes in your files and collaborate with others. You will likely be learning about this in more detail later, but here are some basic commands to get you started:
   - To initialize a new git repository: `git init`
   - To add files to the staging area: `git add filename`
   - To commit changes: `git commit -m "Your commit message"`
   - To view the status of your repository: `git status`
   - To view the commit history: `git log`
3. `sudo`: A command that allows you to run commands with administrative privileges. It stands for "superuser do."
   - To run a command as an administrator: `sudo command`
   - You will be prompted to enter your password.
   - Be careful when using `sudo`, as it can modify system files and settings.
4. If you are on a Linux distribution like Ubuntu, you will likely need `apt`: This is a package manager that allows you to install, update, and remove software packages.
   - To update the package list: `sudo apt update`
   - To install a package: `sudo apt install package_name`
   - To remove a package: `sudo apt remove package_name`
   - Note: You may need to use `sudo` to run these commands with administrative privileges.
5. `brew`: If you are on a Mac, you can use Homebrew, a package manager for macOS.
   - To install Homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
   - To install a package: `brew install package_name`
   - To update Homebrew: `brew update`
   - To upgrade installed packages: `brew upgrade`

There are so many more commands and tools available for you to explore and we definitely cannot list them all here.
We highly encourage you to explore the internet for more tools to help you with your workflow and customize it to be your own!
