Git & GitHub Basics Tutorial (Week 1–2)
This tutorial guides you through the core concepts of version control, installing and configuring Git, understanding the difference between Git and GitHub, and performing essential GitHub operations. By the end, you'll create and push your first GitHub repository.

1. What is Version Control?
Version control is a system that tracks changes to files over time, allowing multiple people to collaborate on a project, revert to previous versions, and maintain a history of modifications. It’s essential for managing codebases, documents, or any project with evolving content.

Why use version control?
Track changes and revert mistakes.
Collaborate with others without overwriting work.
Maintain a history of project evolution.



Example: Imagine editing a document. Version control is like saving snapshots of the document at different stages, so you can go back to an earlier version if needed.

2. Install Git on Your System
Git is a distributed version control system. Follow these steps to install it:
Windows

Download the Git installer from git-scm.com.
Run the installer and accept the default settings.
Verify installation by opening Command Prompt or PowerShell and typing:git --version

You should see something like git version 2.45.2.

macOS

Install Git via Homebrew (recommended):brew install git

Or download the installer from git-scm.com.
Verify installation:git --version



Linux

Install Git using your package manager:
Ubuntu/Debian:sudo apt update
sudo apt install git


Fedora:sudo dnf install git




Verify installation:git --version




3. Configure Git
After installing Git, configure your user information for commit messages.

Open a terminal (Command Prompt, PowerShell, or Terminal).
Set your name:git config --global user.name "Your Name"


Set your email (use the one linked to your GitHub account):git config --global user.email "your.email@example.com"


Verify your configuration:git config --list



Tip: The --global flag sets these settings for all repositories on your system. Omit it to configure a specific repository.

4. Understand the Difference Between Git and GitHub

Git: A local version control system that runs on your computer to track changes in files. It doesn’t require an internet connection.
GitHub: A cloud-based platform for hosting Git repositories, enabling collaboration, code sharing, and remote storage.

Analogy: Git is like a local notebook where you track your work. GitHub is an online library where you store and share that notebook with others.

5. Create a GitHub Account

Go to github.com.
Click Sign Up and follow the prompts to create an account.
Verify your email address.
(Optional) Set up two-factor authentication for security.


6. Initialize a Local Repository
A Git repository is a folder tracked by Git. Let’s create one:

Create a project folder:mkdir my-first-repo
cd my-first-repo


Initialize a Git repository:git init

This creates a hidden .git folder to store version control data.


7. Track Changes
Staging Changes (git add)
The staging area is where you prepare files for a commit.

Create a file, e.g., index.html:echo "<h1>Hello, Git!</h1>" > index.html


Check the status of your repository:git status

You’ll see index.html as an untracked file.
Stage the file:git add index.html

Or stage all files:git add .



Committing Changes (git commit)
A commit is a snapshot of your staged changes.

Commit the staged files with a message:git commit -m "Add index.html with a greeting"

The -m flag adds a commit message describing the changes.


8. View History (git log)
To see the commit history:
git log

This displays a list of commits with their IDs, authors, dates, and messages. Use q to exit the log view.
For a compact view:
git log --oneline


9. Connect to GitHub
To store your local repository on GitHub:

Create a repository on GitHub:

Log in to GitHub.
Click New Repository.
Name it (e.g., my-first-repo).
Choose public or private.
Do not initialize with a README (we’ll push our local repo).
Click Create Repository.
Copy the repository URL (e.g., https://github.com/username/my-first-repo.git).


Link your local repository:In your terminal, connect your local repo to GitHub:
git remote add origin https://github.com/username/my-first-repo.git

Replace the URL with your repository’s URL.

Verify the remote:
git remote -v




10. Push & Pull
Push to GitHub (git push)
Send your local commits to GitHub:
git push -u origin main


-u sets the upstream branch (usually main or master).
You may need to authenticate with your GitHub credentials.

Clone a Repository (git clone)
Download a repository from GitHub to your local machine:
git clone https://github.com/username/my-first-repo.git

This creates a local copy of the repository.
Pull Changes (git pull)
Fetch and merge changes from GitHub to your local repository:
git pull origin main


11. Practice: Create Your First GitHub Repository and Push a Local Project
Let’s combine all the steps into a practical exercise.
Step-by-Step Instructions

Create a project folder:
mkdir my-first-project
cd my-first-project


Initialize a Git repository:
git init


Create and add files:Create a simple README.md:
echo "# My First Project" > README.md

Stage and commit:
git add README.md
git commit -m "Initial commit with README"


Create a GitHub repository:

Go to GitHub and create a new repository called my-first-project.
Do not initialize with a README.
Copy the repository URL.


Connect and push to GitHub:
git remote add origin https://github.com/username/my-first-project.git
git push -u origin main


Verify on GitHub:

Visit your GitHub repository in a browser.
Confirm that README.md appears.


Make changes and push again:Edit README.md:
echo "## About\nThis is my first Git project!" >> README.md

Stage, commit, and push:
git add README.md
git commit -m "Update README with project description"
git push origin main


Clone to another folder (to simulate collaboration):
cd ..
git clone https://github.com/username/my-first-project.git my-first-project-copy




Tips for Success

Commit often: Small, frequent commits make it easier to track changes.
Write clear commit messages: Describe what you changed and why.
Check git status frequently: It helps you understand what’s happening in your repository.
Explore GitHub features: Issues, pull requests, and branches will come in later stages.


Next Steps

Learn about branching (git branch, git checkout).
Explore collaboration workflows (pull requests, forks).
Dive into resolving merge conflicts.

Congratulations! You’ve mastered the basics of Git and GitHub. Keep practicing to build confidence!
