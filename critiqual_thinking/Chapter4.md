# Continuous Delivery for Machine Learning Models

__Questions:__

> Name at least 4 critical checks you can add to verify a packaged model in a container is built correctly.

Within the container, during build:
* Linting
* Tests
* Typechecking

Once the container is built:
* Test endpoints schema
* Snapshot test on a given input

> What are the differences between canary and blue/green deployments? Which one do you prefer? Why?

Canary = direct some of the true production traffic to a new version, blue/green = copy the production traffic to the new version without having customers actually receive results from the new version.
I personally have a preference for blue/green deployment, as the rollout is more flexible, and users will not be affected by any issue with the model that might arise.
The disadvantage of that method is that the new model is not 100% tested in a real environment, as nothing depends on its outputs. But if the system around the model is well designed, this is not a big deal, as as long as the new models respects the schema and the snapshots, serving the customers should be a different concern that is still valid.

> Why are cloud pipelines useful versus using GitHub actions? Name at least three differences.

GitHub actions are a generic tool that has been created to accomodate different use cases. They are therefore not specifically designed with the machine learning use case in mind, where an end-to-end pipeline will have many steps, with potentially complex data sharing / transfer between these steps.
Furthermore, with cloud ML pipelines it's possible to automate the serving of the models, and their deploymemnt.
Finally, pipelines can integrate seamlessly with storage / secrets from within a single cloud provider.

> What does packaging a container mean? Why is it useful?

Packaging a container means providing all the code / infrastructure necessary to build it and run the image. It's useful because it allows anyone to modify it, improve it, and understand how it works, without having to look for specific instructions. Typically, it should have instructions to fetch all external dependencies.

> What are three characteristics of package machine learning models?

Machine learning models require either a model artifact (in the sense of saved weights), or a training part that will generate the model weights.
They further also require to save the metadata that allows to understand how that specific model was trained with what data.
Packaging the model should also make it clear what are the expected inputs / outputs of the model in terms of schema.