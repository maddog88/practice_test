# practice_test

### The process to setup github is similar to gitlab you will either need to configure https authentication or ssh.  We will do https since it is the easiest to understand.  You will need to go into git bash and store a variable locally to tell github your username.  This is the username you created when you first created your github account.
git config user.name "maddog88"
### You will need to store your email as variable locally as well
git config user.email "madmiller8@gmail.com"

### What you typed in gets added in to a config file.  See what you added by adding the below command.  You should be able to see it in the gitconfig file.  If you do not have this file github will not understand who you are.
cat ~/.gitconfig

### Let's create a folder in your User directory.  This is where we will put your repository.
cd ~
mkdir workspace
cd workspace

### To clone the repository down, we are using https to clone it down. 
### Copy the url.  Go into git bash. 
### Type this after the money symbol ($).  The money symbol just expresses you are in the terminal and is the first character you type after.
### example $ git clone <your git repo>
git clone https://github.com/maddog88/practice_test.git
### Behind the scene here is what is happening:  When you run git clone a script is being run behind the scenes to reach out to the url you gave it.  Then github will ask who you are and your computer sends the gitconfig file information.  Next as a final measure of authentication it may ask for your users name and password associated with your github.  Username is maddog88.  The password is the password you told me.


### Change into the directory you have cloned down.  Your repository is essentially just a group of files in a directory.
cd practice_test/

### Now we have are in your repository (aka a the directory with files) that you saved to your your computer.
### You can open visual studio in 2 ways.  You can double click visual studio and open the location you saved the repo. 
### Or you can do it my favorite way.  While in git bash type:
code .
### This says I want to open visual studio with my current directory I am in.

### Now go about making changes to the file firstFile.cs and save changes when you are done.
### I realized .NET is a framework for Windows.  I've never used it.  A framework is a  bunch of different libraries with scripts or another way to describe it.  It's a directory with a bunch of files that are written in C#

### Update your local directory to show to reflect your changes in Visual Studio.
git add .

### Check to see what files you changed. Green will show modified or new files added.  Red will show deleted/removed.
git status

### Commit the code you have added which always requires a message to explain your changes.  This is what you can consider commited or ready to push to github website/server.  The words inbetween the quotes can be whatever you want them to be.
git commit -m "My first Update"

### Add your files to github
git push
### It should pop up a github
