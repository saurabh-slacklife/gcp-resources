# Cloud Run

[Cloud Run](https://cloud.google.com/run/docs), a serverless container runtime, allowing to run stateless container on either Fully managed Cloud Run, GKE Cluster or On-Prem Cloud Run for Anthos.

Build upon [Knative](https://cloud.google.com/knative/) a Kubernetes platform for serverless workloads.

## Concept

### Resource Model

- A service is the main resource of Cloud Run located in a specific region or a GKE cluster namespace.
- A service can have 0 or more container instances serving the requests. A container instance can receive as many concurrent requests as configured under [Concurrency](https://cloud.google.com/run/docs/about-concurrency) with Default maximum of 80.
- Auto-scaling can be 0 or to the max limit set with [maximum number of container instances setting](https://cloud.google.com/run/docs/configuring/max-instances)

> - Irrespective of the Concurrency, if CPU of the instance is highly utilized, Cloud Run might not send as many requests as specified in Concurrency to the instance.
> - The number of instances also depends on the concurrency.
>> - If the Number of Concurrent request is 1 and number of requests served is 3, then 3 instances will be needed and spawned.
>> - If the Number of Concurrent request is 3 or more and number of requests served is 3, then 1 instance will be needed and spawned.
>> - When the Maximum instance limit is reached, any new request queue up for 60 seconds, if it's not processed or taken up by any instance an HTTP 429 error code is returned.
> - Compared to Cloud Functions(Functions-as-a-Service - FaaS), Cloud Functions can only service 1 request at time.

## Resources

### Youtube GCP

1. [Say hello to serverless containers with Cloud Run](https://youtu.be/nhwYc4StHIc)
2. [Migrating Kubernetes apps to Serverless with Cloud Run on Anthos](https://youtu.be/0T5UliS9j8A)

### Qwiklabs

#### Labs
1. [Hello Cloud Run](https://www.qwiklabs.com/focuses/5162?catalog_rank=%7B%22rank%22%3A8%2C%22num_filters%22%3A1%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7363891)
2. [Build a Serverless App with Cloud Run that Creates PDF Files](https://www.qwiklabs.com/focuses/8390?catalog_rank=%7B%22rank%22%3A6%2C%22num_filters%22%3A1%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7363891)
3. [Confluent: Building a Cloud Run Streaming Application with Apache Kafka on Anthos](https://www.qwiklabs.com/focuses/13005?parent=catalog)
4. [Build a Resilient, Asynchronous System with Cloud Run and Pub/Sub](https://www.qwiklabs.com/focuses/8389?catalog_rank=%7B%22rank%22%3A10%2C%22num_filters%22%3A3%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7363902)
5. [Deploy Go Apps on Google Cloud Serverless Platforms](https://www.qwiklabs.com/focuses/10532?parent=catalog)

#### Quests
1. [Google Cloud Run Serverless Workshop](https://www.qwiklabs.com/quests/98?catalog_rank=%7B%22rank%22%3A1%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&search_id=7363816)
2. [Getting Started with Apache Kafka and Confluent Platform on Google Cloud](https://www.qwiklabs.com/quests/145?catalog_rank=%7B%22rank%22%3A3%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&search_id=7363816)
3. [Getting Started with Go on Google Cloud](https://www.qwiklabs.com/quests/129?catalog_rank=%7B%22rank%22%3A20%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379967)