### TODO
* provide at least as much as ryp
* better feedback to the user
  * download progress
  * error message
* install from npm and git
  * first publish without git
* DONE name: im not sure about the S in nmods
  * i prefere to type nmod when i use it
  

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
