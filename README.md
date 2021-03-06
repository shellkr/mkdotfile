## mkdotfile
A simple dotfile manager made in shell-script

#### Description:

**!! Still under heavy development !!**

mkdotfile intend to make managing dotfiles on your system simpler and more automated. Its constuction is simple. It moves the original file to a subfolder, creates a shadow folder structure and then symlinks it back to its originated place. Giving you ability to both use and edit the file as normal. Git will discover when changes have happened to a file in the subfolder and will only add that file to later be pushed.

#### Features:

init, push, restore, tree, track and untrack

#### Usage:

1. Go to your Git service providers web client (like GitHub) and create a new empty repo
2. Run `mkdotfile init` and insert the url of your git repo and name of local dotfile directory
3. Start tracking files with `mkdotfile track /path/to/file`
4. To send changes run `mkdotfile push` and follow instructions.


Run `mkdotfile untrack /path/to/file` if you wish to untrack a file. Make sure this is the same path you first used to track the file. In other words the symlink.

#### Example:

    # This will track xinitrc:
    $ mkdotfile track .xinitrc

    $ mkdotfile tree
    /home/pelle/.dotfiles/dotfiles
       |--[Jun 10 12:13] README.md
       |--[Jun 13 17:20] .xinitrc

    # This will later untrack it:
    $ mkdotfile untrack .xinitrc

If you intend to use the same dotfiles on another machine. You should on that machine run:

1. `mkdotfile init`
2. `mkdotfile restore`
