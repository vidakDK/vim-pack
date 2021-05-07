# How to use

## Initial setup

1. Create directory ~/.vim/pack
2. Initialize git repository:

    git init

3. Configure Vim to search for plugins in that directory with:

    set packpath+=~/.vim/pack/    

4. Add plugins to the pack directory, under `start`, or `opt` or 
   `colours` directory.

5. Set remote, commit, and push.


## Load plugins on new machine
1. `git submodule init`
2. `git submodule update`


## Adding plugins
To add plugins to be always loaded at start, put them in the
`start` directory, if they are optional to be loaded manually
use `opt` directory. Colour related plugins go into `colours` 
directory.


Example of adding an autoloaded plugin:

    git submodule add https://github.com/scrooloose/nerdtree plugins/start/nerdtree
    

## Updating plugins

    git submodule update --remote --merge
    git commit
    git push


## Removing plugins

    git submodule deinit vim/pack/shapeshed/start/vim-airline
    git rm vim/pack/shapeshed/start/vim-airline
    rm -Rf .git/modules/vim/pack/shapeshed/start/vim-airline
    git commit
