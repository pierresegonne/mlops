# MLOps Foundations

TODO: try out cloud shell + VS code in browser. See e.g [here](https://medium.com/google-cloud/how-to-run-visual-studio-code-in-google-cloud-shell-354d125d5748)

AutoML = automatic hyperparemeter tuning, model selection and explainabiltiy.

Greedy algorithm = take best option first.

Data science workflow: Ingest, EDA (exploratory data analysis), Modeling, Conclusion.


__Questions:__

> If GPUs running 24/7, is it worth getting away from the cloud to on-premise?

The premise under which we are answering this question is that the company that runs the GPUs 24/7 is selling GPU databases. This means that the GPUs are at the core of what they are doing. There is probably a potential for drastically reducing costs, and being more flexible with the offering if the company were to transition to on-premise GPUs. If the ability to run a bunch of GPUs is so central to the company's objective, then it can probably invest in making sure that their infrastructure provides similar levels of performance and availability as the cloud providers.

Achieving this level of service would nevertheless be expensive (expensive hardware + physical infrastructure + engineers that can develop such a system are probably very expensive to hire due to the competition from the big tech compagnies), and presents a significant risk. It is probably difficult to assess in advance how much money this change can actually save. Furthermore, this effort will probably reduce the company's agility for experimenting with new offering.

> Why would a managed file service like EFS on AWS or Google FileStore be helpful in a real-world MLOps workflow in corporate America?

These storage systems are known to be extremely reliable, available and cheap. They originally offer the ability to store large amounts of data in an easily accessible fashion, which has proved important for the development of ML applications. They also allow for the implementation of automated pipelines in which intermediary transformations, outputs, images and logs can be stored and manipulated without a prohibitive development or maintenance cost.
For sensitive data, or for larger companies, these file systems are also important to allow ML systems to be compliant. For critical applications such as healthcare, finances, or autonomous driving, it might be critical to hold traces of all data used and transformation applied.

> (Kaizen) Can we do better? What should we do to get better this week or today? How can we apply Kaizen to our machine learning projects?

The output of this exercise reveals some benefits of thinking a ML project in its entirety, with the scope including steps of integration, deployment and serving.
The infrastructure and tooling enforces some level of quality. It does take some time to set everything up, but an improvement could be to script the creation of the entire pipeline. A good boilerplate could provide some strong foundation to then develop any ML project that would be used in practice.