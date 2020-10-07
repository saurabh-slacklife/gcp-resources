# Compute Offerings

# Table of Contents

1. [Serverless](#serverless-(faas))
    - [Cloud Functions (FaaS)](#cloud-functions)
        - [Sample Use Cases](#sample-use-cases)
    - [Cloud Run](#cloud-run)
    - [App Engine Standard Environment](#app-engine-standard-environment) #TODO
2. [Managed Application Platform](#application-platform-(paas)) #TODO
    - [App Engine](#app-engine)
        - [App Engine Standard Environment](#app-engine-standard-environment)
        - [App Engine Flexible Environment](#app-engine-flexible-environment)
3. [Container technology](#containers---containers-as-a-services-(caas)) #TODO
    - [Google Kubernetes Engine (GKE)](#google-kubernetes-engine-(gke))
4. [Virtual Machines (Infrastructure as a Service)](#virtual-machines-(iaas)) #TODO
    - [Compute Instances](#compute-instances)
        - [Preemptible VMs](#preemptible-vms)
        - [Shielded VMs](#shielded-vms)
        - [Sole-Tenant nodes](#sole-tenant-nodes)
4. [Hybrid Cloud Infrastructure](#hybrid-cloud-infrastructure) #TODO
    - [Anthos](#anthos)
5. [Resources](#resources) #TODO

## Serverless (FaaS)

### [Cloud Functions](./compute/serverless/Cloud-Functions.md#cloud-functions)

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

### [Cloud Run](./compute/serverless/Cloud-Run.md#cloud-run)
A serverless container runtime, allowing to run stateless container on either Fully managed Cloud Run, GKE Cluster or On-Prem Cloud Run for Anthos.

## Application Platform (PaaS)

### App Engine

1. Managed Service, Platform as a Service (PaaS), GCP mamages the resources. Hosting, scaling, monitoring and infrastructure.
2. Use pre-defined runtimes or custom runtimes.
3. Supported languages Go, Java, Python, .NET, Node.js, PHP and Ruby.
4. Is located in Multi-regional.

#### [App Engine Standard Environment](./compute/paas/App-Engine-Standard.md)
1. Uses Sandbox instances with supported runtime environments.
2. Instances can scale to 0.
3. No support for websockets.
4. Startup time - within seconds
5. Pricing based upon - Instance hours usage.

#### [App Engine Flexible Environment](./compute/paas/App-Engine-Flexible.md)
1. Uses/Runs container on Compute instances.
2. Runtime is container dependent.
3. Max request timeout - 60 minutes
4. Supports Websocket.
5. Ephemeral storage constrained to compute instance.
6. SSH for debugging.
7. Instance can scale too= - 1.
8. pricing based upon vCpu, memory, persistent disks

## Containers - Containers as a Services (CaaS)

### [Google Kubernetes Engine (GKE)](./compute/caas/GKE.md)

## Virtual Machines (IaaS)

### [Compute Instances](./compute/iaas/Compute-Instances.md#compute-instances)
1. Not managed by GCP.
2. Works on vCPU (which is Hyperthread model).
3. Runs Linux or Windows image which GCP provides or a private Custom images.
4. Use Instance Group to manage multiple instances together, configure autoscaling.
5. Attache Persistent disk - SSD with default AES 256 encryption or HDD with default AES 128 encryption. Has a default boot persistent disk
6. Can also run Docker containers on [Container-Optimized](https://cloud.google.com/container-optimized-os/docs) OS image.
7. Each VM belongs to one VPC and instances in same network communicate through Local area network.
8. The default TZ of VM is UTC.

#### [Preemptible Vms](./compute/iaas/Preemtible-Vms.md)

#### [Shielded Vms](./compute/iaas/Shielded-Vms.md)

#### [Sole-Tenant nodes](./compute/iaas/Sole-Tenant-Nodes.md)

#### [Cloud GPUs](./compute/iaas/Cloud-GPUs.md)

## Hybrid Cloud Infrastructure

### [Anthos](./compute/hybrid/Anthos/md)

## Resources
[Top 3 ways to run your Containers on Google Cloud](https://youtu.be/jh0fPT-AWwM)



