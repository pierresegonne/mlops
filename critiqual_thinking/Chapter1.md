# Chapter 1 - Introduction to MLOps

__Questions:__

> What problems does a CI system solve?

First, a CI system allows to integrate new changes on the codebase automatically. As soon as code is accepted by the peer review process, the CI system takes over to ensure that this new piece of code is integrated smoothly. This means that humans can focus on where they bring value: architecture, and implement.
A system CI furthermore offers assurances for the practical runnability of the newly integrated code. The automatic execution of tests, and the building of the application on different platforms can for example be used to make sure that the code will run as expected once deployed.
Finally, it is also worth integrating formatting and linting tools within the CI to ensure code style consistency and code quality.

A CI system therefore relies on a number of basic principles that must be, at least in parts, be implemented before the CI. These include test coverage, a proper peer-reviewed code reviewing process, version control, and infrastructure to run the CI.

> Why is a CI system an essential part of a both a SaaS software product and an ML system?

A SaaS product must respect some sort of contract with its end users. This contract must hold some sort of quality assurance, and one of the steps in the process must be to make sure that the integration of new code is validated and ran automatically, while being reproducible.

Code is one of the three key components of any ML system. For this reason alone, a CI system must be integrated in any ML system. In this case, the CI could cover other areas as well, such as data and metadata.

> Why are cloud platforms the ideal target for analytics applications? How do data engineering and DataOps assist in building cloud-based analytics applications?

On cloud platforms, storage access, and data discrimination is facilitated.

Data engineering and DataOps should focus on building up the infrastructure that makes the data readibly available, in a coherent format, with quality safeguards for seamless integration and analytics.

> How does deep learning benefit from the cloud? Is deep learning feasible without cloud computing?

Cloud application can easily access reliable distributed computing resources. This makes the execution of any heavy training process safer, but also faster. Additionally, many deep learning projects depend on multiple parameters, and their training must be ran multiple times to select the best parameters. Running everything on a cloud platform forces the practicioner to design his experiment tracking and configuration system in a way that is easy to monitor and that ensures reproducibility.

> Explain what MLOps is and how it can enhance a ML engineering project?

MLOps is the application of DevOps processes to systems that involve some ML components. MLOps can be divided from DevOps as it involves creating processes for handling the integration and usability of not only code, but also data and metadata/configuration.

In a ML engineering project, MLOps will facilitate multiple stages of the project's life: from tracking the experiments that will help select the best model, to making sure that the data fed into the model respects the requirements, to making sure that the model does not become stale to enventually automating the deployment of the model.
