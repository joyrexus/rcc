# RCC Services Group

We develop web and data services for research initiatives at the University of Chicago with the aim of furthering open, transparent, reproducible research.

---

The role of the RCC Services Group is to help research teams transform the data they collect during the lifecycle of their project into useful research datasets.  We help shape, extend, and preserve high-value data collections, making them available to a wider research community.

Our users typically have large collections of data gathered at various stages of their research efforts.  Some of the data they collect is potentially useful for future research, much of it is not.  For any high-value collections, we work with them to distill, document, and expose their data in a meaningful way.

For our purposes, a **research dataset** consists of the following components:

* *store* - a structured datastore
* *api* - a restful api exposing this collection
* *docs* - describing the datastore's schema and api
* *views* - various web-based views on the data
  * *filters* - a simple query interface
  * *dashboards* - aggregate views; simple visualization and reporting tools
* *controls* - authentication and permissions for restricting access


## Workflow

A typical project typically moves through the following stages:

* preliminaries - where we clarify the service we provide
* requirements - where we gather specs
* design - where we propose some initial ideas
* prototyping - where we cook up some working prototypes
* deployment - where we deploy the api and expose views
* maintenance - where we undertake initial maintenance


## Preliminaries

Make clear up front what we deliver: a structured research dataset tailored
to a specific research community.  To make clear what we mean by a research
dataset, walk through [a working example](http://harvest.research.chop.edu/demo/) from a previous project.


## Requirements

We first want to clarify the audience and scope of the project.

Who is the audience for this dataset?  Which researchers might use this dataset?  Are these researchers located within the university community?  

Authentication/Permissions: will users need differentiated levels of access to the data?
