# Git Cheat Sheet

Here is a compact version of my Git cheat sheet:


## Frequently Used Commands

- `git init`: Initialize a new Git repository
- `git clone <repo>`: Clone a repository
- `git log --graph --oneline --decorate --all`: Show commit history as a graph in a compact format with decorations for all branches
- `git status`: Show the working tree status
- `git add <file>`: Add file to staging area
- `git commit -m "message"`: Commit changes with a message
- `git branch <branch>`: Create a new branch
- `git checkout <branch>`: Switch to a branch
- `git merge <branch>`: Merge a branch into the current branch
- `git pull`: Fetch and merge changes from the remote repository
- `git push`: Push changes to the remote repository


## Basic Commands

- `git init`: Initialize a new Git repository
- `git clone <repo>`: Clone a repository
- `git add <file>`: Add file to staging area
- `git commit -m "message"`: Commit changes with a message
- `git status`: Show the working tree status
- `git log`: Show commit history
- `git diff`: Show changes between commits, commit and working tree, etc.
- `git branch`: List, create, or delete branches
- `git checkout <branch>`: Switch to a branch
- `git merge <branch>`: Merge a branch into the current branch
- `git pull`: Fetch and merge changes from the remote repository
- `git push`: Push changes to the remote repository


## Git Logs and Status

- `git status`: Show the working tree status
- `git log`: Show commit history
- `git log --oneline`: Show commit history in a compact format
- `git log --graph`: Show commit history as a graph
- `git log --stat`: Show commit history with statistics about changes
- `git log --author=<author>`: Show commit history filtered by author
- `git log --grep=<pattern>`: Show commit history filtered by a specific pattern in the commit message
- `git log --since=<date>`: Show commit history since a specific date
- `git log --until=<date>`: Show commit history until a specific date
- `git log --patch`: Show commit history with the changes introduced in each commit
- `git log --pretty=format:"%h - %an, %ar : %s"`: Show commit history with a custom format
- `git log --name-only`: Show commit history with the names of changed files
- `git log --name-status`: Show commit history with the names and status of changed files
- `git log --follow <file>`: Show commit history for a specific file, including renames
- `git log --all`: Show commit history for all branches
- `git log --graph --oneline --all`: Show commit history as a graph in a compact format for all branches
- `git log --graph --oneline --decorate`: Show commit history as a graph in a compact format with decorations for all branches
- `git log --graph --oneline --decorate --all`: Show commit history as a graph in a compact format with decorations for all branches


## Branching and Merging

- `git branch <branch>`: Create a new branch
- `git checkout <branch>`: Switch to a branch
- `git merge <branch>`: Merge a branch into the current branch
- `git rebase <branch>`: Reapply commits on top of another base tip
- `git cherry-pick <commit>`: Apply the changes introduced by some existing commits 
- `git stash`: Stash changes in a dirty working directory
- `git stash pop`: Apply stashed changes and remove them from the stash list
- `git stash list`: List all stashed changes
- `git stash apply`: Apply stashed changes without removing them from the stash list
- `git stash drop`: Remove a stashed change from the stash list
- `git stash clear`: Remove all stashed changes

## Remote Repositories

- `git remote add <name> <url>`: Add a new remote repository
- `git remote -v`: List remote repositories
- `git fetch <remote>`: Fetch changes from a remote repository
- `git pull <remote> <branch>`: Fetch and merge changes from a remote branch
- `git push <remote> <branch>`: Push changes to a remote branch
- `git remote remove <name>`: Remove a remote repository
- `git remote rename <old> <new>`: Rename a remote repository
- `git remote set-url <name> <url>`: Change the URL of a remote repository
- `git remote show <name>`: Show information about a remote repository
- `git remote update`: Fetch updates for all remotes
- `git remote prune <name>`: Remove remote-tracking references that no longer exist on the remote
- `git remote set-head <name> <branch>`: Set the default branch for a remote repository
- `git remote get-url <name>`: Get the URL of a remote repository
- `git remote set-url --push <name> <url>`: Set the push URL for a remote repository
- `git remote set-url --add <name> <url>`: Add a new URL to a remote repository
- `git remote set-url --delete <name> <url>`: Remove a URL from a remote repository
- `git remote set-url --push --add <name> <url>`: Add a new push URL to a remote repository
- `git remote set-url --push --delete <name> <url>`: Remove a push URL from a remote repository


## Undoing Changes

- `git reset --soft <commit>`: Move HEAD to a specific commit, keeping changes
- `git reset --mixed <commit>`: Move HEAD to a specific commit, unstaging changes
- `git reset --hard <commit>`: Move HEAD to a specific commit, discarding
- `git revert <commit>`: Create a new commit that undoes the changes of a specific commit
- `git clean -f`: Remove untracked files from the working directory
- `git clean -fd`: Remove untracked files and directories from the working directory
- `git clean -n`: Show which files would be removed by `git clean`
- `git clean -x`: Remove untracked files, including ignored files
- `git clean -X`: Remove only ignored files
- `git clean -e <pattern>`: Exclude files matching the pattern from being removed
- `git clean -i`: Interactive mode for cleaning untracked files
- `git clean -d`: Remove untracked directories in addition to untracked files
- `git clean -q`: Suppress output of removed files
- `git clean -v`: Show verbose output of removed files
- `git clean -f -d`: Forcefully remove untracked files and directories
- `git clean -f -x`: Forcefully remove untracked files, including ignored files
- `git clean -f -X`: Forcefully remove only ignored files
- `git clean -f -e <pattern>`: Forcefully remove untracked files, excluding files matching the pattern
- `git clean -f -i`: Forcefully remove untracked files in interactive mode
- `git clean -f -q`: Forcefully remove untracked files without showing output
- `git clean -f -v`: Forcefully remove untracked files with verbose output


## Configuration

- `git config --global user.name "Name"`: Set the name for commits
- `git config --global user.email "email@example.com"`: Set the email for commits
- `git config --global core.editor <editor>`: Set the default text editor
- `git config --global merge.tool <tool>`: Set the default merge tool
- `git config --global diff.tool <tool>`: Set the default diff tool
- `git config --global alias.<alias> <command>`: Create a shortcut for a

    Git command
- `git config --global --edit`: Edit the global Git configuration file
- `git config --global --list`: List all global Git configuration settings
- `git config --global --get <key>`: Get the value of a specific global Git configuration setting
- `git config --global --unset <key>`: Unset a specific global Git configuration setting
- `git config --global --unset-all <key>`: Unset all values for a specific global Git configuration setting
- `git config --global --replace-all <key> <value>`: Replace all values for a specific global Git configuration setting with a new value
- `git config --global --add <key> <value>`: Add a new value for a specific global Git configuration setting
- `git config --global --get-regexp <pattern>`: Get all global Git configuration settings that match a specific pattern
- `git config --global --get-color <key> <default>`: Get the color value for a specific global Git configuration setting, or return a default value if the setting is not defined
- `git config --global --get-colorbool <key> <default>`: Get the boolean value for a specific global Git configuration setting, or return a default value if the setting is not defined
- `git config --global --get-colorbool <key>`: Get the boolean value for a specific global Git configuration setting, or return false if the setting is not defined
- `git config --global --get-colorbool <key> true`: Get the boolean value for a specific global Git configuration setting, or return true if the setting is not defined
- `git config --global --get-colorbool <key> false`: Get the boolean value for a specific global Git configuration setting, or return false if the setting is not defined
- `git config --global --get-colorbool <key> auto`: Get the boolean value for a specific global Git configuration setting, or return auto if the setting is not defined
- `git config --global --get-colorbool <key> always`: Get the boolean value for a specific global Git configuration setting, or return always if the setting is not defined
- `git config --global --get-colorbool <key> never`: Get the boolean value for a specific global Git configuration setting, or return never if the setting is not defined
- `git config --global --get-colorbool <key> default`: Get the boolean value for a specific global Git configuration setting, or return default if the setting is not defined


## Aliases

- `git config --global alias.co checkout`: Create an alias for the `checkout` command
- `git config --global alias.br branch`: Create an alias for the `branch` command
- `git config --global alias.ci commit`: Create an alias for the `commit` command
- `git config --global alias.st status`: Create an alias for the `status` command
- `git config --global alias.last 'log -1 HEAD'`: Create an alias for showing the last commit
- `git config --global alias.unstage 'reset HEAD --': Create an alias for unstaging changes
- `git config --global alias.visual '!gitk --all &': Create an alias for visualizing the commit history with gitk
- `git config --global alias.graph 'log --oneline --graph --all': Create an alias for showing the commit history in a graph format
- `git config --global alias.lg 'log --oneline --graph --decorate': Create an alias for showing the commit history in a graph format with decorations
- `git config --global alias.lg1 'log --oneline --graph --decorate --all': Create an alias for showing the commit history in a graph format with decorations for all branches
- `git config --global alias.lg2 'log --oneline --graph --decorate --all --abbrev-commit': Create an alias for showing the commit history in a graph format with decorations for all branches and abbreviated commit hashes
- `git config --global alias.lg3 'log --oneline --graph --decorate --all --abbrev-commit --color': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, and colored output
- `git config --global alias.lg4 'log --oneline --graph --decorate --all --abbrev-commit --color=auto': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, and colored output that is automatically enabled or disabled based on the terminal's capabilities
- `git config --global alias.lg5 'log --oneline --graph --decorate --all --abbrev-commit --color=always': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, and colored output that is always enabled
- `git config --global alias.lg6 'log --oneline --graph --decorate --all --abbrev-commit --color=never': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, and colored output that is never enabled
- `git config --global alias.lg7 'log --oneline --graph --decorate --all --abbrev-commit --color=default': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, and colored output that is enabled or disabled based on the default settings
- `git config --global alias.lg8 'log --oneline --graph --decorate --all --abbrev-commit --color=auto --date=relative': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, colored output that is automatically enabled or disabled based on the terminal's capabilities, and relative date formatting
- `git config --global alias.lg9 'log --oneline --graph --decorate --all --abbrev-commit --color=auto --date=iso': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, colored output that is automatically enabled or disabled based on the terminal's capabilities, and ISO date formatting
- `git config --global alias.lg10 'log --oneline --graph --decorate --all --abbrev-commit --color=auto --date=local': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, colored output that is automatically enabled or disabled based on the terminal's capabilities, and local date formatting
- `git config --global alias.lg11 'log --oneline --graph --decorate --all --abbrev-commit --color=auto --date=relative --author=<author>': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, colored output that is automatically enabled or disabled based on the terminal's capabilities, relative date formatting, and filtering by a specific author
- `git config --global alias.lg12 'log --oneline --graph --decorate --all --abbrev-commit --color=auto --date=relative --grep=<pattern>': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, colored output that is automatically enabled or disabled based on the terminal's capabilities, relative date formatting, and filtering by a specific pattern in the commit message
- `git config --global alias.lg13 'log --oneline --graph --decorate --all --abbrev-commit --color=auto --date=relative --author=<author> --grep=<pattern>': Create an alias for showing the commit history in a graph format with decorations for all branches, abbreviated commit hashes, colored output that is automatically enabled or disabled based on the terminal's capabilities, relative date formatting, and filtering by both a specific author and a specific pattern in the commit message


## Tips

- Use `git help <command>` to get detailed information about a specific command
- Use `git <command> --help` to get detailed information about a specific command
- Use `git <command> -h` to get a brief summary of a specific command
- Use `git <command> --version` to check the version of Git you are using
- Use `git <command> --verbose` to get more detailed output for a specific command
- Use `git <command> --quiet` to suppress output for a specific command
- Use `git <command> --dry-run` to see what a command would do without actually performing the action
- Use `git <command> --force` to force a command to run, even if it may have unintended consequences
- Use `git <command> --no-edit` to skip the commit message editor when committing changes
- Use `git <command> --amend` to modify the most recent commit
- Use `git <command> --no-verify` to bypass pre-commit and commit-msg hooks when committing changes
- Use `git <command> --signoff` to add a "Signed-off-by" line to the commit message
- Use `git <command> --author="Name <email>"` to specify the author of a commit
- Use `git <command> --date="date"` to specify the date of a commit
- Use `git <command> --allow-empty` to create an empty commit
- Use `git <command> --allow-empty-message` to create a commit with an empty commit message
- Use `git <command> --no-allow-empty` to prevent creating an empty commit
- Use `git <command> --no-allow-empty-message` to prevent creating a commit with an empty commit message
- Use `git <command> --reset-author` to reset the author information for a commit
- Use `git <command> --reset-author --no-edit` to reset the author information for a commit without opening the commit message editor
- Use `git <command> --reset-author --amend` to reset the author information for the most recent commit
- Use `git <command> --reset-author --amend --no-edit` to reset the author information for the most recent commit without opening the commit message editor
- Use `git <command> --reset-author --amend --no-allow-empty` to reset the author information for the most recent commit and prevent creating an empty commit
- Use `git <command> --reset-author --amend --no-allow-empty-message` to reset the author information for the most recent commit and prevent creating a commit with an empty commit message
- Use `git <command> --reset-author --amend --no-allow-empty --no-allow-empty-message` to reset the author information for the most recent commit and prevent creating an empty commit or a commit with an empty commit message 

