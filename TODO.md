### BUGS

* nmod install notexistingpkg  do a crash...

### TODO

* allow a search
  * curl "http://search.npmjs.org/_view/search?startkey=%22express%22&endkey=%22expressZZZZZZZZZZZZZZZZZZZ%22&reduce=false"
  * http://wiki.apache.org/couchdb/HTTP_view_API#Querying_Options for docs
* complete npm install url
  * support tar+zip
  * support any url but be better when you can (e.g. github url)
* support git too ? well maybe but later. currently tar/zip will do
  * can i do a specific github
  * like using github api instead of npmjs one
  * to fix the version flexibility of fixed tar
  * something like "tags" == all available versions
* better report for nmod list ?
  * currently this is like a ls -R
  * something like express (qs, connect(qs))
   jerome@jmebox:/tmp/slota$ nmod list
   ./node_modules/express
   ./node_modules/express/node_modules/connect
   ./node_modules/express/node_modules/connect/node_modules/qs
   ./node_modules/express/node_modules/qs
   jerome@jmebox:/tmp/slota$ express (sq, connect(qs))
   
### DONE
   
* DONE better feedback to the user
  * download progress
  * error message
* DONE possible to put url in dependancies. but only .tgz, but github is tar ok
  * maybe find a shortcut like this
  * github to get the tgz... not perfect at all... but workable now
  * in fact nmod should support a tgz as source of package
  * this is like the usual install without the version resolution
  * nmod install express
  * nmod install express '>= 0.0.3'
  * nmod install http://github.com/slota.tgz
  * nmod install https://github.com/isaacs/npm/tarball/v0.3.9
* DONE issue in the async of install
  * i install all deps at the same time
  * may be faster but disturb the user (and who care about speed in install)
  * unsure i did some work. not sure on the status but seems to work
* DONE do the native package compilation
  * rm -rf ./build && node-waf configure && node-waf build
* DONE put the semver in nmod file
* DONE name: im not sure about the S in nmods
  * i prefere to type nmod when i use it

### VISION
* provide simple way to install packages
  * standalone
  * only install package at userlevel
    * no plist, upstart, /usr/bin and all
* install from npm and git
  * first version npm only
  * git version later
    * only based on package.json and git repo
    * thus to publish and all is out of nmod scope


### NOTES (wondering if not too complex)
  
* i loved node_modulew design
  * regular, simple yet powerfull
* package.json dependencies
  * one from node modules
  * one from nmods
* how to offer a pure git solution?
  * something ignored by npm and accepted by nmods
  * somthing which give a way to ref module by their git url
* need simple instruction for packager to support it

### DONE

* FIXED still some bugs in install with deps
  * nmods install express <- how to reproduce it
  * i think this is due to the bugs in the async
    * like i remove before updating
* DONE make it reccursive
  * port it
* DONE find a good name
  * nmods - node_modules from npm or git
    * this one seems cool
    * moto is clear and short
    * it is short and node.js users like this
    * git source makes it different from npm/ryp
    * DECIDED
