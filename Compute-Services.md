# Compute Services

## [Serverless](#serverless)
## [Managed Application Platform](#application-platform-(paas))
## [Container technology](#containers---containers-as-a-services-(caas))
## Hybrid Cloud Infrastructure

## [Serverless](https://youtu.be/PBw9vD_BO5A)

### Cloud Functions (FaaS)

1. Functions as a Service (FaaS), provides serverless execution environment for building and connecting Cloud Services.
2. The functions are attached/watched to the Events fired/triggered/emitted by Cloud Infrastructure.
3. Supported languages:
   a. Javascript - Nodejs 10 execution env
   b. Python - Python3 based on 3.7
   c. Go - Go 1.11or 1.13
   d. Java - Java 11
   
#### Sample Use Cases:
1. ETL and Data Processing through Pub/Sub events. IoT streaming, Audio/Video streaming, Data encryption etc.
2. Webhooks for HTTP events.
3. Lightweight Loosely coupled stateless APIs.
4. Mobile backend functions.

### [Cloud Run](./Cloud-Run.md#cloud-run)
A serverless container runtime, allowing to run stateless container on either Fully managed Cloud Run, GKE Cluster or On-Prem Cloud Run for Anthos.

## Application Platform (PaaS)

### App Engine

1. Managed Service, Platform as a Service (PaaS), GCP mamages the resources. Hosting, scaling, monitoring and infrastructure.
2. Use pre-defined runtimes or custom runtimes.
3. Supported languages Go, Java, Python, .NET, Node.js, PHP and Ruby.
4. Is located in Multi-regional.

#### App Engine Standard Environment
1. Uses Sandbox instances with supported runtime environments.
2. Instances can scale to 0.
3. No support for websockets.
4. Startup time - within seconds
5. Pricing based upon - Instance hours usage.

#### App Engine Flexible Environment
1. Uses/Runs container on Compute instances.
2. Runtime is container dependent.
3. Max request timeout - 60 minutes
4. Supports Websocket.
5. Ephemeral storage constrained to compute instance.
6. SSH for debugging.
7. Instance can scale too= - 1.
8. pricing based upon vCpu, memory, persistent disks

## Containers - Containers as a Services (CaaS)

### Google Kubernetes Engine (GKE)

### Virtual Machines (Infrastructure as a Service)

### Compute Instances
1. Not managed by GCP.
2. Works on vCPU (which is Hyperthread model)
3. Use Instance Group to manage multiple instances together, configure autoscaling.
4. Attache Persistent disk - SSD with default AES 256 encryption or HDD with default AES 128 encryption.

### Resources
[Top 3 ways to run your Containers on Google Cloud](https://youtu.be/jh0fPT-AWwM)


