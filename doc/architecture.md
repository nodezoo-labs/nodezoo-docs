Back to [TOC](../Readme.md)

![Nodezoo][Logo]

# Architecture

Nodezoo is a search engine for node modules. The full system currently fetches data from NPM, Github and Travis-CI. It is an example of a real-world service built using Node.js micro-services. Each micro-service is published in its own github repository along with all of the necessary config to run the system locally or live . The codebase is intended to be used as an example, and as a starting point for your own projects.

![Diagram](https://github.com/nodezoo/nodezoo-docs/blob/master/img/architecture.jpeg)

Each microservice is saved in its own repository. The list of microservices and a short description is presented below:

 * [WEB](https://github.com/nodezoo/nodezoo-web) - NodeZoo Front End (Using React/Redux/Webpack)
 * [Search](https://github.com/nodezoo/nodezoo-search) - NodeZoo Search micro-service. Updates ElasticSearch and also is used to query Elasctic search according with WEB requests
 * [Info](https://github.com/nodezoo/nodezoo-info) - NodeZoo Search micro-service. Handles module information.
 * [NPM](https://github.com/nodezoo/nodezoo-npm) - NodeZoo micro-service used to query NPM for modules information.
 * [Github](https://github.com/nodezoo/nodezoo-github) - NodeZoo micro-service used to query Github for modules information.
 * [Travis](https://github.com/nodezoo/nodezoo-travis) - NodeZoo micro-service used to query Travis for modules information.
 * [Coveralls](https://github.com/nodezoo/nodezoo-coveralls) - NodeZoo micro-service used to query Coveralls for modules information.
 * [Dequeue](https://github.com/nodezoo/nodezoo-dequeue) - NodeZoo micro-service. A message dequeuer for NodeZoo
 * [Updater](https://github.com/nodezoo/nodezoo-updater) - NodeZoo micro-service that subscribe to NPM for module notifications. Also able to get list with all modules published in npm.
 * [Base](https://github.com/nodezoo/nodezoo-base) - Seneca Mesh Base used by NodeZoo application.
 
Other useful repositories:
 * [System](https://github.com/nodezoo/nodezoo-system) - Shows how to deploy locally NodeZoo application - production or development environments
 * [Terraform](https://github.com/nodezoo/nodezoo-terraform) - Contains Terraform configuration files for deploying NodeZoo on AWS, each microservice in a Docker container, in separate instances.
 * [Org](https://github.com/nodezoo/nodezoo-org) - A place for org resources and discussions around Nodezoo.
 


[Logo]: https://raw.githubusercontent.com/nodezoo/nodezoo-org/master/assets/logo-nodezoo.png
