# nmod

nmod is a [node_modules](http://nodejs.org/docs/v0.4.1/api/modules.html#loading_from_node_modules_Folders)
manager.

node_modules is a [0.4 new feature](https://github.com/joyent/node/blob/v0.4.0/ChangeLog#L5).
It provides a simple and regular way to install packages (read
[more](http://nodejs.org/docs/v0.4.1/api/modules.html#loading_from_node_modules_Folders)).
nmods is cloned from [ryp](https://github.com/isaacs/ryp) but is implemented in node.js.
Thanks to *node_modules* principle, *nmod* installs npm packages locally.

## How to use it ?

To install express in ./node_modules

    nmod install express
    
To list all packages installed in ./node_modules

    nmod ls

To remove express

    nmod rm express

All commands

    nmod install <package> - Install a package, and nest its deps.
    nmod ls                - Show installed packages.
    nmod rm <package>      - Remove a package
    nmod deps              - Install dependencies from package.json file

## How to install it ?

*nmod* is a [single node file](http://github.com/jeromeetienne/nmod/raw/master/nmod), so easy to install

    sudo wget -O /usr/bin/nmod --no-check-certificate http://github.com/jeromeetienne/nmod/raw/master/nmod
    sudo chmod +x /usr/bin/nmod
