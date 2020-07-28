![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Labs | Getting started with GIT and GITHUB

In this document, you will find all the steps you should follow when working on git and github (in the prework and during the bootcamp).

## Step 1: Steps For Installing Git for Windows

**Prerequisites**
- Administrator privileges
- Access to a command-line
- Your favorite coding text editor
- Username and password for the Github

**Download Git for Windows**

1. Browse to the official Git website: https://git-scm.com/downloads
2. Click the download link for Windows and allow the download to complete.
![](https://i1.faceprep.in/ProGrad/git-1.png)

**Extract and Launch Git Installer**

3. Browse to the download location (or use the download shortcut in your browser). Double-click the file to extract and launch the installer.
![](https://i1.faceprep.in/ProGrad/git-2.png)

4. Allow the app to make changes to your device by clicking Yes on the User Account Control dialog that opens.
![](https://i1.faceprep.in/ProGrad/git-3.png)

5. Review the GNU General Public License, and when you’re ready to install, click Next.
![](https://i1.faceprep.in/ProGrad/git-4.png)

6. The installer will ask you for an installation location. Leave the default, unless you have reason to change it, and click Next.
![](https://i1.faceprep.in/ProGrad/git-5.png)

7. A component selection screen will appear. Leave the defaults unless you have a specific need to change them and click Next.
![](https://i1.faceprep.in/ProGrad/git-6.png)

8. The installer will offer to create a start menu folder. Simply click Next.
![](https://i1.faceprep.in/ProGrad/git-7.png)

9. Select a text editor you’d like to use with Git. Use the drop-down menu to select Notepad++ (or whichever text editor you prefer) and click Next.
![](https://i1.faceprep.in/ProGrad/git-8.png)

10. This installation step allows you to change the PATH environment. The PATH is the default set of directories included when you run a command from the command line. Leave this on the middle (recommended) selection and click Next.
![](https://i1.faceprep.in/ProGrad/git-9.png)

11. The next option relates to server certificates. Most users should use the default. If you’re working in an Active Directory environment, you may need to switch to Windows Store certificates. Click Next.
![](https://i1.faceprep.in/ProGrad/git-10.png)

12. The next selection converts line endings. It is recommended that you leave the default selection. This relates to the way data is formatted and changing this option may cause problems. Click Next.
![](https://i1.faceprep.in/ProGrad/git-11.png)

13. Choose the terminal emulator you want to use. The default MinTTY is recommended, for its features. Click Next.
![](https://i1.faceprep.in/ProGrad/git-12.png)

14. The default options are recommended, however this step allows you to decide which extra option you would like to enable. If you use symbolic links, which are like shortcuts for the command line, tick the box. Click Next.
![](https://i1.faceprep.in/ProGrad/git-13.png)

15. Depending on the version of Git you’re installing, it may offer to install experimental features. At the time this article was written, the option to include interactive options was offered. Unless you are feeling adventurous, leave them unchecked and click Install.
![](https://i1.faceprep.in/ProGrad/git-14.png)

16. Once the installation is complete, tick the boxes to view the Release Notes or Launch Git Bash, then click Finish.
![](https://i1.faceprep.in/ProGrad/git-15.png)








### How to fork?

<small>All the examples will be related to your ProGrad journey, and they will point to the [`FACEPrep-ProGrad`](https://github.com/FACEPrep-ProGrad
) GitHub organization. </small>

Navigate to the repository you want to fork. Let's take an example of the prework [HTML exercise](https://github.com/FACEPrep-ProGrad/project-builder-html-css-npm).

![](https://i1.faceprep.in/ProGrad/1.png)

After clicking on the fork button, you will be presented with the loading screen that will most likely look like this:

![](https://i1.faceprep.in/ProGrad/2.png)

After the forking is done successfully, you will be redirected to the **copied repository on your GitHub account**.

![](https://i1.faceprep.in/ProGrad/3.png)

We are done here with the forking process.

## Step 2: Clone the repository

Now, on your GitHub account, you have access to the copied repository. This will be repository you will copy (clone) to your local machine, and that will be your working area.

### How to clone repository?

1. Click on the green ‘Clone or download’ button and copy the link by selecting and copying or by using the clipboard button.

![](https://i1.faceprep.in/ProGrad/4.png)

2. Open your terminal and navigate to the location where you want to store the local version of your repository.
3. When you navigated to the correct folder in your terminal run the following command:

```shell
$ git clone <paste url from the clipboard>
```

Check the image below if you have any doubts:

![](https://i1.faceprep.in/ProGrad/5.png)

4. Once the cloning process is done, you see the following information in your terminal. And you can check that repository was successfully cloned from GitHub to your local machine by running `ls` command in your terminal:

![](https://i1.faceprep.in/ProGrad/6.png)

The cloning process is finished with this step. Now you can use the code to make changes before we proceed to the next step, which is pushing the changes to the forked repository on your GitHub.

### Using cloned repository locally

Before you open the project, you have to navigate into the cloned folder because that’s where `git` is initialized:

```shell
$ cd <name of cloned folder >
```

To open the project in VS Code, you have to run the following command when you already navigated to the folder:

```shell
$ code .
```

If in doubt, check the following image:

![](https://i1.faceprep.in/ProGrad/7.png)

Now we are ready to start working/making changes. Quickly go to the terminal and, while in the copied repository, run the following command:

```shell
$ git status
```

![](https://i1.faceprep.in/ProGrad/8.png)

This shows us that there were no changes made locally, yet.

## Step 3: Add, commit and push the changes

After you made changes to your project, you can check which files you changed by running again:

```shell
$ git status
```

![](https://i1.faceprep.in/ProGrad/9.png)

### How to add changes?

Currently, we demoed making changes to a single file. You might be making changes to one or multiple files; thus, you might see many files marked as _modified_.

In case you want to add just one file and you are not ready to add the others, you can do so with the following command:

```shell
$ git add <name of the file>
```

![](https://i1.faceprep.in/ProGrad/10.png)

However, most likely, you would like to add all the changes so that you will use the following command more often:

```shell
$ git add .
```

<small> :+1: The dot represents all files in the current repository.</small>

![](https://i1.faceprep.in/ProGrad/11.png)

### How to commit changes?

After all changed files are added, you should commit your files and add a commit message describing the things you have changed, with the following command:

```shell
$ git commit -m “<your message>”
```

![](https://i1.faceprep.in/ProGrad/12.png)

### How to push changes?

After committing your changes, you can push the commits from your local machine to your remote repository on GitHub with the following command:

```shell
$ git push origin master
```

![](https://i1.faceprep.in/ProGrad/13.png)

Perfect! The changes we made are now available in the remote repository on our GitHub profile.

Now, let's go to the GitHub and learn how to make the pull request.

## Step 4: Create a pull request

After pushing your changes from your local master to the remote master, your commit should be visible on GitHub (the changes you made locally are now available in GitHub repository as well).

When your commit is successfully pushed to GitHub, you can create a pull request by clicking on the "New pull request" button.

![](https://i1.faceprep.in/ProGrad/14.png)

After clicking on that button, you will be forwarded to the following page:

![](https://i1.faceprep.in/ProGrad/15.png)

As you can see in the image above, when you initialize the process for creating the pull request, you will be redirected to the original repository (where you were at the very beginning when you started the process of forking).

The final step is just to fill out the pull request title and the body.

![](https://i1.faceprep.in/ProGrad/16.png)

By pressing the green “Create pull request” button, you will create the pull request to the original lab repository.

### The final

If you would click on the "Pull requests", you will see your own pull request:

![](https://i1.faceprep.in/ProGrad/17.png)

<br><br>

**That would be it. Happy Coding ProGrad ❤️!**
