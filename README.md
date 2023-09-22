# smiths-project

If faced any issue with denied permission delete git credentials in keychain and do ssh again, or remove security credentials if you're using windows.(Google)

## Set these defaults first before initializing a git repository.

```bash
# Set your global Git username
git config --global user.name "Your Name"
# Set your global Git email address
git config --global user.email "Your Email"
# Configure Git to use the "simple" push strategy
git config --global push.default simple
# Create a Git alias for 'checkout'
git config --global alias.co checkout
# Set the default branch name for new repositories to 'main'
git config --global init.defaultBranch main
# Initialize a new Git repository with the 'main'
```

## To initialize repository

```bash
git init -b main
# Connect your local repository to a remote repository
git remote add origin your_git_repo_link
# Stage all changes in your working directory
git add .
# Create an initial commit with a descriptive message
git commit -am "initial commit"
# Push your local 'main' branch to the 'main' branch on the remote repository
git push -u origin main
```

# Requirements to run next.js project:

- Node.js
- npm

# to run project, enter npm run dev
