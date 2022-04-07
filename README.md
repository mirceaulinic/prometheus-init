# prometheus-init

Initialise Prometheus registry from a given datasource

## Why?

In theory, Prometheus metrics should be assumed that they are volatile. However, in some specific cases, Counters may be useful at their absilute values besides applying a function, e.g., ``rate()`` on them. For these specific (and rare) cases, you might feel like you need your counters to keep counting even after an application restart. Here's where ``prometheus-init`` may help you: it provides an API for you to load your metrics (that you have dumped into a file or another system) into a registry, and from there you can continue the usual metrics manipulation.
