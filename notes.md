# Notes

Notes and references for immediate needs.

* [rcc wiki](https://w3.rcc.uchicago.edu/redmine/projects/rcc/wiki/Wiki)
* [intro guide](http://docs.rcc.uchicago.edu/user-guide.html)
* [intro tutorial](http://docs.rcc.uchicago.edu/tutorials/intro-to-rcc-workshop.html)
* [more tutorials](http://docs.rcc.uchicago.edu/tutorials/index.html)


## Utilities

* `id` - print real and effective user and group IDs
* `usertool` - add, modify, delete, or show entries in the LDAP server
* `phldap` - queries the UChicago LDAP server


## Software builds

* [modules tutorial](http://docs.rcc.uchicago.edu/tutorials/modules.html) for existing builds
* [details on the build process](https://w3.rcc.uchicago.edu/redmine/projects/rcc/wiki/Software_build_process_changes)


## Static file hosting

It is possible to serve files from `$HOME/public_html` on Midway. The associated URL will be `http://users.rcc.uchicago.edu/~CNETID`.

For this to work you need to make your home directory accessible (`/bin/chmod
o+rx /home/$USER`).
