# MLOps for Containers and Edge Devices

Containers VS virtual machine: Containers are all about the application itself, and only what the application is versus what it needs to run. Virtual machines are all-in-one services where the db, web server and any other system service are installed.

Anytime one wants to create a container, there must be a Dockerfile in the directory.

One of the many useful aspects of containers is that they can be composed of many layers, and these layers can be used or reused in other containers.

Note on repositories/tags: `docker build -t REPOSITORY:TAG .`

Note on running a container: `docker run --rm -it --d REPOSITORY:TAG`. `--rm` removes the container after stopping it. `-it` allocates a TTY, which emulates a terminal and attaches stdin to it.

Direct access to bash within the container: `docker exec -it SHA bash`.

`hadolint` can be used to lint the Dockerfile.

`grype` can do vulnerability scanning.

Deploying to the edge means deploying to compute devices that are not within a data center, e.g mobile phone, raspberry pi, smart home device etc.

Note that with containers, there is a possibility for monetisation of models. Cloud marketplaces allow to sell containerised models, given their specs, as a product.

__Questions:__

> What is a container runtime, and how does it relate to Docker?

The container runtime is the software that is needed to run a container within a system. It was created by Docker.

> Name three good practices when creating a Dockerfile.

Docker operates in layers, so it is important to organise the dockerfile so we don't add useless layers that would inflate the image's size without a reason. Dockerfile should be linted, dependencies versioned and the built image should be verified for vulnerabilities.

> What are two critical concepts of DevOps mentioned in this chapter? Why are they useful?

Automation & Sharing. Containers are a great implementation of these two concepts, they can automate the building and deployment of pieces of code as micro services. These containers can then be shared through the registry. That allows for the aggregation of knowledge, and systems to accelerate development and operations.