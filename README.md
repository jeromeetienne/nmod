# nmod

nmod is a [node_modules](http://nodejs.org/docs/v0.4.1/api/modules.html#loading_from_node_modules_Folders)
packages installer.

node_modules is a [0.4 new feature](https://github.com/joyent/node/blob/v0.4.0/ChangeLog#L5).
It provides a simple and regular way to install packages (read
[more](http://nodejs.org/docs/v0.4.1/api/modules.html#loading_from_node_modules_Folders)
). nmods is cloned on [ryp](https://github.com/isaacs/ryp) but is implemented in node.js.
Thanks to *node_modules* principle, **nmod** installs npm packages locally.

## How to use it ?

to install express in ./node_modules

    nmod install express
    
to list all packages installed in ./node_modules

    nmod ls

to remove express

    nmod rm express

all commands

    nmod install      - Install a package, and nest its deps.
    nmod ls           - Show installed packages.
    nmod rm           - Remove a package
    nmod deps         - Install dependencies from package.json file

## How to install it ?

nmod is a single executable file, so easy to install

    curl http://github.com/jeromeetienne/nmod/raw/master/nmod > /usr/bin/nmod
    chmod +x /usr/bin/nmod
