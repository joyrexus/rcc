# Demos

Demos of data-discovery web apps customized for a particular domain.

* [Harvest + OpenMRS](http://harvest.research.chop.edu/demo/) - nice demo 
  of the [Harvest Stack](http://harvest.research.chop.edu/), a toolkit 
  designed by and for biomed researchers.

The following are smaller and more focused examples demonstrating how [crossfilter](https://github.com/square/crossfilter/wiki) and [dc.js](http://dc-js.github.io/dc.js/) can enable interactive exploration of multivariate datasets (both large and small) in the browser.

* [Airline on-time performance](http://square.github.io/crossfilter/) - this is the original [crossfilter](https://github.com/joyrexus/crossfiltering) demo.

* [UC Trends](http://saraquigley.github.io/uc-trends/) - a clean and 
  simple front-end for exploring University of California Revenue and 
  Expense Trends.

* [Canadian Crime Stats](http://dc-js.github.io/dc.js/crime/index.html) - clean and simple front-end for exploring Canadian crime stats.

* [Recline Demos](http://okfnlabs.org/recline/demos/) - a set of examples
  demonstrating the data exploration features provided by the
  [recline.js](http://okfnlabs.org/recline/) client-side library.


---


## Domain Specific Platforms


### [Harvest](http://harvest.research.chop.edu/)

I *really* like [the vision behind Harvest](http://harvest.research.chop.edu/manifesto/), but the Django-based architecture is a non-starter for us.


### [Palladio](http://palladio.designhumanities.org/)

The Stanford Humanities + Design team created this web-based platform for the visualization of complex, multi-dimensional data.  The current interation appears to be targeting spatial datasets, but many components of this project could help enable interactive visualization analysis of non-spatial datasets.  

For background and design details, see [this post](http://esjewett.com/blog/palladio) by the chief architect.


### [CKAN](http://ckan.org)

An open-source data portal platform primarily targeting civic data.  It's a
python framework (using the Pylons web framework and SQLAlchemy ORM) with a postgres backend.  The framework provides exposes a web interface for basic data exploration tasks.  It also exposes an extensive [RESTful JSON API](http://docs.ckan.org/en/latest/api/index.html) for developers, enabling them to access and query hosted datasets via an HTTP client.

A CKAN host can serve as a backend for a frontend client library, such as [recline.js](http://okfnlabs.org/recline/docs/), enabling the development of custom data-discovery interfaces.
