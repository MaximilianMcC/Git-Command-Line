# Git Command Line Interface
This is a test repository for learning how to use Git in Git Bash. All of the steps that I used are below


### **1 - Make a repo**
Before we do anything in the command we need to make a repo. Go to the GitHub website and create a new repo. Don't add a readme as we will be adding this later on using Git Bash. Name it whatever you want and copy the url because we will need this later.

### **2 - Make or open your code**
Open Git Bash and move to where your code is located or where you are going to write your code. Here is an example of making a new folder for my code:
```sh
# Go to my programming folder
cd Documents/Code/Website/

# Make a new folder and go into it
mkdir git-cli
cd git-cli
```

### **3 - Initialize the Git Repository**
Now we are going to make this folder our Git repo.
```sh
# Initialize the Git Repository
$ git init
```
From this you should see something that says `Initialized empty Git repository in <PATH TO YOUR CODE>`

### **4 - Add a readme file**
Adding a readme file lets people get information about your repository. First run this to make one
```sh
# Create a new file called `README.MD`
touch README.MD

# Edit the file
nano README.MD
```
Now you should see an ascii art text editor in your terminal. Write this in it:
```
# Git Command Line Stuff

This was made using Git Bash
```
After that then press `ctrl+s` to save then `ctrl+x` to exit. Now all we need to do is add the file to the repo:
```sh
# Add the file
git add README.MD
```

### **5 - Commiting your changes**
Now we can commit our changes.
```sh
# Commit evrything with a message
git commit -m "Added first files"
```

### **6 - Push evrything to GitHub**
The last thing that we need to do is push our changes. This will upload all of our code and files to GitHub under your repository. To do this we need to move into the main branch:
```sh
# Move into the main branch
git branch -M main
```
Now when looking at your prompt in Git Bash the text at the end should have changed from `master` to `main`. After we are in main we can move into the repo on GitHub.
```sh
# Replace <REPO URL> with the url we coppied at the start of the tutorial
# Example: git remote add origin https://github.com/MaximilianMcC/Git-Command-Line.git
git remote add origin <REPO URL>.git
```
The final step is to upload our files to GitHub:
```sh
# Upload the files that we comitted to the main branch
git push -u origin main
```

### **7 - Done**
Now we have succesfully added files to GitHub with Git Bash using a cli. Whenever you need to add more code use this:
```sh
# Add your new code
# If you put `--all` instead of a filename it will add everything
git add --all

# Commit all changes
git commit -m "Added and changed files"

# Push the files to your GitHub repo
git push -u origin main
```

Example of adding a HTML and CSS file to a repo:
```sh
# Make and edit the HTML file
touch index.html
nano index.html

# Make and edit the CSS file
touch style.css
nano style.css

# Add them both to GutHub
git add --all
git commit -m "Added HTML and CSS files"
gut push origin main
```