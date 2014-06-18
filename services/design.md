# Architecture

Some initial notes.


## API design

Read through the [CKAN API docs](http://docs.ckan.org/en/latest/api/index.html) as a nice example of how a rich RESTful API could be developed.  They provide both a read and a write API (for authorised users).

See the [dat API](https://github.com/maxogden/dat/blob/master/docs/api.md) for
something much more simple and streamlined.


## Client-side MVC

On the client-side of things, look at how [recline.js](http://okfnlabs.org/recline/docs/) uses [backbone](http://backbonejs.com/) for MVC.
