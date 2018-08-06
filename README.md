# we1s-cloud

`we1s-cloud` is a collection of services for supporting the WhatEvery1Says project. It uses [Docker](https://www.docker.com/) containers via compose/swarm, managed via the [Portainer](https://portainer.io/) web UI.

Services include:

-  [we1s-collector](https://github.com/whatevery1says/we1s-collector)  
   An agent for assembling collections of documents, with task queue and api interfaces.  Uses [lexis-nexis-wsk] and [PySiQ](https://github.com/fikipollo/PySiQ).
   -  [we1s-collector-ui](https://github.com/whatevery1says/we1s-collector-ui)  
      Web interfaces to `collector`.

-  [we1s-manager](https://github.com/whatevery1says/we1s-manager)  
   The Workflow Management System (WMS). A web portal to manage document collections and their sources (along with associated metadata) and generate WE1S projects. A python [Flask](http://flask.pocoo.org/) web application with [MongoDB](https://www.mongodb.com/) storage
   -  [we1s-manager-db](https://github.com/whatevery1says/we1s-db)  
      NoSQL database for `manager`. MongoDB

-  [we1s-notebook](https://github.com/whatevery1says/we1s-notebook)  
   Analysis and visualization notebooks.  Uses [Jupyter](http://jupyter.org/), built on the [datascience stack](https://github.com/jupyter/docker-stacks/tree/master/datascience-notebook), with [mallet](http://mallet.cs.umass.edu/) for topic modeling, and [dfr-browser](https://github.com/agoldst/dfr-browser) for visualization.
   -  [we1s-notebook-viewer](https://github.com/whatevery1says/we1s-viewer)  
      A simple webhost for browsing information visualization website outputs from `notebook`. Uses [nginx](https://www.nginx.com/).

