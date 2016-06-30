# mkdotfile
A simple dotfile manager made in shell-script

Description

mkdotfile intend to make managing dotfiles on your system simpler and more automated. Its constuction is simple. It moves the original file to a subfolder, creates a shadow folder structure and then symlinks it back to its originated place. Giving you ability to both use and edit the file as normal. Git will discover when changes have happened to a file in the subfolder and will only add that file to later be pushed.

Features
init, push, restore, track and untrack

