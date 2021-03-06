# Tools

Core tools used by the RCC Services Group.


## Node 

RCC Web Services leverages [Node](http://nodejs.org/) as a platform for easily building fast, scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications.  It enables rapid development of both HTTP+JSON APIs as well as native web apps via [browserify](http://browserify.org/).


## Server-side

* [hapi](http://hapijs.com/) - web services framework
* [seaport](https://github.com/substack/seaport) - service registry and port
  assignment

#### database

* [dat](https://github.com/maxogden/dat) - an API for reading, writing and syncing datasets
* [level-db](http://leveldb.org/) - flexible, lightweight persistence
* [rethink-db](http://rethinkdb.com/) - nosql datastore
* [mysql](https://github.com/felixge/node-mysql#mysql) - mysql bindings for
  node
* [sqlite3](https://github.com/mapbox/node-sqlite3) - sqlite3 bindings for node


## Client-side

* [ampersand.js](http://ampersandjs.com/) - modular MV\* framework for
  client-side data-manipulation and view rendering
* [level.js](https://github.com/maxogden/level.js) - leveldb for the browser
* [npm-dom](https://github.com/npm-dom) - basic inventory of DOM modules

#### ui-design

* [bootstrap-examples](http://getbootstrap.com/getting-started/#examples)
* [bootsnip](http://bootsnipp.com/) - bootstrap-based design elements
* [button-builder](http://bootsnipp.com/buttons)
* [form-builder](http://minikomi.github.io/Bootstrap-Form-Builder/)

#### data manipulation

* [nest.js](https://github.com/joyrexus/nest) - for data nesting and rollups
* [crossfilter.js](http://square.github.io/crossfilter/) - fast
  multidimensional filtering for coordinated views

#### utilities

* [minimist.js](https://github.com/substack/minimist) - arg parsing
* [browserify.js](http://browserify.org/) - for packaging up modules

##### visualization

* [dc.js](http://dc-js.github.io/dc.js/) - crossfilter-driven charting
* [epoch.js](http://fastly.github.io/epoch/) - real-time charting lib w/
* [cubism.js](https://square.github.io/cubism/) - a D3 plugin for visualizing
  time series, enabling better realtime dashboards unified styling


## Reference

* [art-of-node](https://github.com/maxogden/art-of-node#the-art-of-node) -
  nice overview of the node ecosystem
* [human-js](http://read.humanjavascript.com/ch01-introduction.html) - best
  practices for building native HTML5 apps
* [http-api-design](https://github.com/interagent/http-api-design) - best
  practices for the design of an HTTP+JSON API
* [finding-modules](http://substack.net/finding_modules) - recommended
  principles for evaluating npm packages
* [dat-modules](https://github.com/maxogden/dat/blob/master/docs/modules.md) -
  descriptions of modules used in the `dat` project
* [tape-is-cool](http://www.macwright.org/2014/03/11/tape-is-cool.html) - nice article explaining why we should use the TAP protocol 
* [how-i-write-tests](http://substack.net/how_I_write_tests_for_node_and_the_browser) - test harness for node and browsers

