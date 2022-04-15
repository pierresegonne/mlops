# AutoML and KaizenML

AutoML = focused strictly on creating the best model possible from clean data
KaizenML = improving everything about the machine learning process. Example: being data centric, and focusing on improving data quality lives under KaizenML

On the issue of data science vs autoML vs kaizenML. The first is a behaviour, looking within data to find trends / patterns that be valuable for a given problem. AutoML is a technique for finding the best parameters for a model, and kaizenML is a process for improving the delivery of value from ML models.

Feature stores do two things:
* Allow users to add features they built into a shared feature store.
* Once features are in the feature store, they are easy to use in training and prediction.

__Questions:__

> Why is AutoML only part of the automation story with modern machine learning?

There are a few enablers for autoML that I believe only appeared quite recently. The improvements in computing power, and the learnings from real world usage of ML has allowed to generate a framework for automatically training multiple models with different hyperparameters without prohibitive costs.
The second part of the answer lies in the necessity to integrate ML models with production environmnets. While previous ML model where at the intersection between scientific research and industry, and were custom created, the generalisation of machine learning has created the opportunity for applying the same types of models for different use cases. For these cases, the people having to integrate the models within the production environment realise that most of the complexity does not actually lie in the training of the model itself, but rather creating the infrastructure to support it. This therefore creates a need for being able to automatically and quickly train a model, that will then be carefully integrated.

> How could the NIH (National Institue of Health) use a feature store to increase the speed of medical discoveries?

The creation of such public feature store would enable multiple practicioners to experiment with new kinds of models to uncover patterns and analyse the open data. This could directly generate some insights for new medical discoveries, but it could also have the indirect effect of providing information back to the NIH about what kinds of data are the most important to careful track and register.

> By 2025, what parts of ML will be fully automated and what will not? Same in 2035?

By 2025, model training and deployment will be mostly automatic. By 2035, feature engineering and storing should also be automated. I clearly envision a path, where from a data store, the simple specification of what kind of targets are needed will automatically train and serve a model.

The role of humans will probably be limited to making sure that the data is correctly served to the data store, and on the research for new model types.

> How could vertically integrated AI platforms (chips, frameworks, data and more) give particular companies a competitive edge?

We've seen how recently how the specialisation of hardware led to sharp improvements in the execution speed of models, and allowed the integration of more complex and better performing models. With vertical integration, these companies can control the level of complexity of models being used in their platforms, and potentially outcompete their competitors with ML powered features impossible to copy on other devices. Providing the framework for seamless integration of ML in applications that are fed to these platforms will decouple this effect.

> How does the chess software industry provide insights into how AI and humans work together in solving problems for autoML?

No idea mate.

> How does a data-centric approach differ from a model-centric approach to machine learning? How about a KaizenML approach where data, software, and modeling are all treated as equally important?

Data-centric = focus efforts on improving the processes of data manipulations, resulting in e.g better quality data and more robust processes. Model-centric focuses on improving the quality of the models that operate on that data. KaizenML can be seen as a generalisation of both concepts, where everything that deals with data and modeling is to be continuously improved.
