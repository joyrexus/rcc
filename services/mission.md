# Mission

RCC Services Group statement of purpose.

Our role is to aid research teams at the University of Chicago that would like to repurpose (preserve, extend, and amplify) their high-value data collections into vehicles for data-discovery for targeted research needs.  

While the RCC and Computation Institute have long provided data management and
high-performance computing services (i.e., general data/computational infrastructure services independent of any particular research domain), our focus will be on developing custom data-discovery capabilities for specific research communities. 

---

We help University research teams transform the data they've collected in the course of some project (with a particular analytical objective) into an explorable research dataset that's tailored to the specific needs of a research community (with perhaps quite different analytical objectives) extending beyond the team that initially collected the data.  The targeted community may be future members of an internal team, an interdisciplinary team within the University, or a larger and more distributed community of researchers.

In short, we aim to repurpose high-value data collections for new forms of data-discovery.


## Process

We want to de-couple the data modeling and view specification process from the api and web app development process.

We utilize the original team's domain expertise and knowledge of the underlying
data collection to create a structured data model.  We then gather use cases
and conduct a needs assessment from the targeted research community to
get a rough picture of how they'd ideally like to explore this data model.

With the data model articulated, we can then integrate the available data collections into a backend datastore.  We expose the resulting datastore through a restful api.  With the resulting data endpoints, we can then develop rich client-side data-exploration tools (i.e., customized query interfaces) targeted to the needs of a particular set of users (future researchers with analytical objectives perhaps quite distinct from the original research team that collected the underlying data).
