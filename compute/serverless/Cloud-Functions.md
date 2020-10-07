# Cloud Functions

## Concepts

1. Each instance of a function handles only one concurrent request.
2. To cater multiple concurrent requests, cloud Functions spawns multiple instances based on the number of requests. Hence each function instance doesn't share any memory, variables, cpu. 
3. A limit can be set on the number of instances which should be spawned at  a given time. [Max Instances](https://cloud.google.com/functions/docs/max-instances)
4. Default timeout of request is 60 seconds, but can be configured to maximum of 9 minutes.

The function is executed on the associate triggers on a created Event.

Supported Events:
- HTTP
- Cloud Storage
- Cloud Pub/Sub
- Cloud Firestore
- Firebase
- Stackdriver logging - by creating a sink to Cloud Pub/Sub topic

## Resources

[List of use cases](https://cloud.google.com/functions/docs/tutorials)

## Qwiklabs

### Labs
1. [Cloud Functions: Qwik Start - Console](https://www.qwiklabs.com/focuses/1763?catalog_rank=%7B%22rank%22%3A2%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
2. [Cloud Functions: Qwik Start - Command Line](https://www.qwiklabs.com/focuses/916?catalog_rank=%7B%22rank%22%3A3%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
3. [Google Assistant: Build an Application with Dialogflow and Cloud Functions](https://www.qwiklabs.com/focuses/3634?catalog_rank=%7B%22rank%22%3A4%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
4. [Monitoring and Logging for Cloud Functions](https://www.qwiklabs.com/focuses/1833?catalog_rank=%7B%22rank%22%3A5%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
5. [HTTP Google Cloud Functions in Go](https://www.qwiklabs.com/focuses/5171?catalog_rank=%7B%22rank%22%3A6%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
6. [Ingesting Data Into The Cloud Using Google Cloud Functions](https://www.qwiklabs.com/focuses/12637?catalog_rank=%7B%22rank%22%3A7%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
7. [Serverless Compute: Microservices with Cloud Functions](https://www.qwiklabs.com/focuses/8498?catalog_rank=%7B%22rank%22%3A8%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
8. [Responding to Stackdriver Messages with Cloud Functions](https://www.qwiklabs.com/focuses/8500?catalog_rank=%7B%22rank%22%3A10%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367269)
9. [Clean Up Unused IP Addresses](https://www.qwiklabs.com/focuses/7841?catalog_rank=%7B%22rank%22%3A13%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367309)
10. [Clean Up Unused and Orphaned Persistent Disks](https://www.qwiklabs.com/focuses/7797?catalog_rank=%7B%22rank%22%3A14%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367309)
11. [Optimizing Cost with Google Cloud Storage](https://www.qwiklabs.com/focuses/7830?catalog_rank=%7B%22rank%22%3A15%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367309)
12. [Using Cloud Logging with IoT Core Devices](https://www.qwiklabs.com/focuses/2768?catalog_rank=%7B%22rank%22%3A16%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367309)
13. [Serverless Compute: Microservices with Cloud Functions](https://www.qwiklabs.com/focuses/8498?catalog_rank=%7B%22rank%22%3A2%2C%22num_filters%22%3A3%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7367344)

### Quests

1. [Getting Started with Go on Google Cloud](https://www.qwiklabs.com/quests/129?catalog_rank=%7B%22rank%22%3A20%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379967)

## Youtube

- [Google Cloud Functions](https://youtu.be/1r3vMYywNLk)
- [Cloud Functions quickstart](https://youtu.be/vM-2O-uKBNQ)
- [Run Cloud Functions Everywhere (Cloud Next '19)](https://youtu.be/yMEcyAkTliU)