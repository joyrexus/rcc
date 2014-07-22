# Notes

Notes and references for immediate needs.

* [rcc wiki](https://w3.rcc.uchicago.edu/redmine/projects/rcc/wiki/Wiki)
* [intro guide](http://docs.rcc.uchicago.edu/user-guide.html)
* [intro tutorial](http://docs.rcc.uchicago.edu/tutorials/intro-to-rcc-workshop.html)
* [more tutorials](http://docs.rcc.uchicago.edu/tutorials/index.html)
* [slurm docs](https://computing.llnl.gov/linux/slurm/)


## Quick facts

* The number of nodes on Midway varies per partition
* The primary partition is `sandyb` with ...
  * 275 nodes
  * 16-cores per node
* Each user is allowed to have ...
  * 96 simultaneous jobs 
  * 1536 cores allocated to their jobs


## Quick tips


#### Useful utilities

* `id` - print real and effective user and group IDs
* `usertool` - add, modify, delete, or show entries in the LDAP server
* `phldap` - queries the UChicago LDAP server
* [rcchelp](https://w3.rcc.uchicago.edu/redmine/projects/rcc/wiki/Rcchelp_User_Guide) - in-house python wrapper around various utility commands


#### Add/modify group membership

Check a user's group membership:

    id CNET_ID

Add a user to a group: 

    usertool groupmod -m USER GROUP

List members of a group:

    rcchelp group-members GROUP


#### Check CNetID status

Use `phldap` to see if a user has a CNetID:

Search for a user by name:

    phldap FIRST LAST

Search for a user by CNetID:

    phldap uid=cnetid


#### User account approval

Users can request accounts through the [account request form](http://rcc.uchicago.edu/user_documentation/general_user_account_request.html).

See [this article](https://w3.rcc.uchicago.edu/redmine/projects/rcc/wiki/Account_Approval_Process) in the redmine wiki for an overview of the approval process.

To manually approve an account that has been submitted use the [rt ticketing
system](https://rt.rcc.uchicago.edu/rt/):  

* use the righthand **Quick Search** menu to identify account request tickets
* click on a ticket
* click the **Basics** tab
* set **account-verified** to `true`
* set **approve-ticket** to `true`


#### Software builds

* [modules tutorial](http://docs.rcc.uchicago.edu/tutorials/modules.html) for existing builds
* [details on the build process](https://w3.rcc.uchicago.edu/redmine/projects/rcc/wiki/Software_build_process_changes)


#### Static file hosting

It is possible to serve files from `$HOME/public_html` on Midway. The associated URL will be `http://users.rcc.uchicago.edu/~CNETID`.

For this to work you need to make your home directory accessible (`/bin/chmod
o+rx /home/$USER`).


