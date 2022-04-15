# Monitoring and Logging

Snippet for python logging:

```
log_format = "[%(name)s][%(levelname)-6s] %(message)s"
logging.basicConfig(format=log_format)
logger = logging.getLogger(__name__)
logget.setLevel(...)
```

The bus test = Can I get hit by a bus today, and have everything still work, and everyone that works with me being able to pick up the slack.

__Questions:__

> Why might it be desirable to log to multiple sources at the same time?

Reliability and scalability. Persistance of logs is very important for controlling the execution of the systems, and log processing systems might be multiple. Having a unique storage for logs introduces a single failure point that will most likely be used when the system in not behaving as expected.

> Why is it critical to monitor data drift?

Data drift might arise as soon as the data being fed is outside of our control. Typical example would be processing data we receive about user behaviour. If the user data is pre-processed, upstream, any change on that processing might induce data drift in what is the input data for the model, with unanticipated consequences.

> Name three advantages of using logging facilities versus `print()` or `echo` statements?

- Logging does not stop execution, and provides useful traceback information.
- Allows filtering of the logged messages depending on the verbosity
- Can be persisted easily into a file

> List the five most common log levels from least to most verbose

- _CRITICAL_
- _ERROR_
- _WARNING_
- _INFO_
- _DEBUG_

> What are three common metri types found in metric capturing systems?

- _timer_: Monitors the execution time of a process
- _value_: Monitors a given value that represents a piece of the system. Ex: size of processed dataset.
- _count_: Increases in value by one everytime monitoring is triggered.
