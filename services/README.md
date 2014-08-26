# RCC Services Group

We develop web and data services for research initiatives at the University of Chicago with the aim of furthering open, transparent, reproducible research.

---

**The role of the RCC Services Group is to help research teams transform the data they collect during the lifecycle of their project into useful research datasets.**  We help shape, extend, and preserve high-value data collections, making them available to a wider research community.  Our aim is to promote innovative data-reuse and discovery.

Our users typically have large collections of data gathered at various stages of their research efforts.  Some of the data they collect is potentially useful for future research, much of it is not.  For any high-value collections, we work with them to distill, document, and expose their data in a meaningful way.
Our role is to help them expose these data collections in a way that promotes discovery, enabling future researchers to more easily query these collections without being forced to think in terms a relational model and SQL statements.

While we do aim to enable *high-level* data exploration and reporting, the
principal function of our tooling around the dataset is to make it easy for
researchers to filter and select the data of interest required for a particular
analysis, which they would then export/download in a format suitable for whatever tools they're most comfortable with to carry out their final modeling and/or analysis.


## Deliverables

A **research dataset** should be understood to consists of the following elements:

* *store* - a structured datastore
* *api* - a restful api exposing this collection
* *docs* - structured documentation describing the datastore's schema and api
* *views* - various web-based views on the data
  * *filters* - a simple query interface
  * *dashboards* - aggregate views; simple visualization and reporting tools
* *controls* - authentication and permissions for restricting access


## Process

We intend to develop a standard process and framework for quickly constructing
such custom research datasets where 80% of the code base is comprised of re-usable components. The remaining 20% is for customization of the components based on the particular needs of the project.

We want to de-couple the data modeling and view specification process from the api and web app development process.

We utilize the original team's domain expertise and knowledge of the underlying
data collection to create a structured data model.  We then gather use cases
and conduct a needs assessment from the targeted research community to
get a rough picture of how they'd ideally like to explore this data model.

With the data model articulated, we can then integrate the available data collections into a backend datastore.  We expose the resulting datastore through a restful api.  With the resulting data endpoints, we can then develop rich client-side data-exploration tools (i.e., customized query interfaces) targeted to the needs of a particular set of users (future researchers with analytical objectives perhaps quite distinct from the original research team that collected the underlying data).


## Workflow

A typical project typically moves through the following stages:

* preliminaries - where we clarify the service we provide
* requirements - where we gather specs
* design - where we propose some initial ideas
* prototyping - where we cook up some working prototypes
* deployment - where we deploy the api and expose views
* maintenance - where we undertake initial maintenance


#### Preliminaries

Make clear up front what we deliver: a structured research dataset tailored
to a specific research community.  To make clear what we mean by a research
dataset, walk through [a working example](http://harvest.research.chop.edu/demo/) from a previous project.

Note that there are many stages in the construction of a research dataset. The
RCC Services Group we'll typically get involved with a project after the bulk
of the research data has been collected, though we should be willing to advise
projects on their data collection efforts.  We'll most likely be involved in the data integration and schema definition efforts, but this will be guided by the particular use cases envisioned by our clients.  In other words, we're principally focused on the developing data exploration and general reporting tools for pre-existing data collections, where the tools are targeted at a specific audience of future reseachers.  We need to be very clear with our clients that they'll need to articulate the needs of these future users.  


#### Requirements

We first want to clarify the audience and scope of the project.

Who is the audience for this dataset?  Which researchers might use this dataset?  Are these researchers located within the university community?  

Once our client has a defined audience in mind, they'll be in a better position
to articulate how these future researchers might want to sift, filter, and aggregate the underlying dataset.

Authentication/Permissions: will users need differentiated levels of access to the data?


## Tools

See our list of standard [tools](tools.md).


## Inspiration

* [palladio](http://palladio.designhumanities.org/) - Stanford
  humanities+design project for visualizing multi-dimensional datasets.
* [harvest](http://harvest.research.chop.edu/) - toolkit for building web apps
  for integrating, discovering, and reporting data.
* [CKAN]() - framework for publishing datasets with a rich RESTful JSON API.
* [recline.js](http://okfnlabs.org/recline/) client-side library for
  developing simple data exploration interfaces.
