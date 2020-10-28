# Git-demo
Building git proficiency

## Setting up git

1. Download and install:  
> brew install git

#If you already have Git installed, you can get the latest development version via Git itself:  
> git clone https://github.com/git/git

2. Setting your username in Git:  
> git config --global user.name "Mansi Gupta" (#for every repository on computer)
> 
> git config --global user.name (# to check the user name)
> 
> git config user.name "Mansi Gupta" (#for a single repository)


## Create a new repo

1. Use the github website for this.
2. Add README when creating a new repo.

## Making changes/creating a branch

1. If you make any changes to a file there are two options:
    - to update in the existing/master branch
    - to create a new branch
2. After creating a new branch, you can create a new pull request.
3. After working on it, you can merge the pull request to the master branch if everything works well in your current branch.
4. Doing this merges all the files from this branch to the master and closes this branch with an option to delete it.

### Pull Request

Create a pull request to propose and collaborate on changes to a repository. These changes are proposed in a branch, which ensures that the default branch only contains finished and approved work.

### Merging

1. In a pull request, you propose that changes you've made on a head branch should be merged into a base branch.
2. If you decide you don't want the changes in a topic branch to be merged to the upstream branch, you can close the pull request without merging.

#### Merging options:
1. **Merge all of the commits into the base branch (DEFAULT)**:
    all commits from the feature branch are added to the base branch in a merge commit
2. **Squash the commits into one commit**:
    the pull request's commits are squashed into a single commit. Instead of seeing all of a contributor's individual commits from a topic branch, the commits are combined into one commit and merged into the default branch.
3. **Rebase the commits individually onto the base branch**:
    all commits from the topic branch (or head branch) are added onto the base branch individually without a merge commit. Pull requests with rebased commits are merged using the fast-forward option.
    
## Fork a repo

A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

Method:
- Fork the repository.
- Make the fix.
- Submit a pull request to the project owner.

Uses:
- Propose changes to someone else's project
- Use someone else's project as a starting point for your own idea.

## Cloning a repo

Cloning is downloading all the files in a repository to your local computer for you to work on. There are several ways in which cloning can be done.
1. Just download the zip file
2. Use HTTPS (When you git clone, git fetch, git pull, or git push to a remote repository using HTTPS URLs on the command line, Git will ask for your GitHub username and password. )
3. Use SSH (SSH URLs provide access to a Git repository via SSH, a secure protocol. When you git clone, git fetch, git pull, or git push to a remote repository using SSH URLs, you'll be prompted for a password and must provide your SSH key passphrase.)

### Connecting to GitHub with SSH

Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username or password at each visit.

1. [Checking for existing SSH keys](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/checking-for-existing-ssh-keys)
2. [Generating a new SSH key](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
3. [Adding a new SSH key to your GitHub account](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

> ls -al ~/.ssh
>
> ssh-keygen -t rsa -b 4096 -C "your_email_id@something.com"
>
> eval "$(ssh-agent -s)"
>
> open ~/.ssh/config
>
> touch ~/.ssh/config
>
> ssh-add -K ~/.ssh/id_rsa
>
> pbcopy < ~/.ssh/id_rsa.pub
>
> Go to the settings page on GitHub and add your key by pasting the information on clipboard after the above command.
                  
## Go to commands

**To setup a project:**     
> git clone <CLOUD_REPOSITORY_CLONE_URL(SSH)>

**For an existing project**     
> git init
>
> git remote add origin <CLONE_URL>

**Status**      
> git status

**Branch**
> git checkout -b <new_branch_name>

**To switch to an existing branch**     
> git checkout <branch_name>

**Pushing**     
> git add .
>
> git commint -m "<commint_message>"
>
> git push origin <branch_name>

#### For a quick git guide:
https://training.github.com/downloads/github-git-cheat-sheet/

- **git clone** means you are making a copy of the repository in your system.

- **git fork** means you are copying the repository to your Github account.

- **git pull** means you are fetching the last modified repository.

- **git push** means you are returning the repository after modifying it.

