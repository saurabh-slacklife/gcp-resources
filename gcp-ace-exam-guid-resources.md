# 1. Setting up a cloud solution environment
## 1.1 Setting up cloud projects and accounts. Activities include:
- Creating projects
    - Qwiklabs
    - GCP Docs

- Assigning users to predefined IAM roles within a project
    - Qwiklabs
    - GCP Docs
- Managing users in Cloud Identity (manually and automated)
    - Qwiklabs
    - GCP Docs
- Enabling APIs within projects
    - Qwiklabs
    - GCP Docs
- Provisioning one or more Stackdriver workspaces
    - Qwiklabs
    - GCP Docs

##  1.2 Managing billing configuration. Activities include:
- Creating one or more billing accounts
    - Qwiklabs
    - GCP Docs
- Linking projects to a billing account
    - Qwiklabs
    - GCP Docs
- Establishing billing budgets and alerts
    - Qwiklabs
    - GCP Docs
- Setting up billing exports to estimate daily/monthly charges
    - Qwiklabs
    - GCP Docs

## 1.3 Installing and configuring the command line interface (CLI), specifically the Cloud SDK (e.g., setting the default project).
- Qwiklabs
- GCP Docs

# 2. Planning and configuring a cloud solution

## 2.1 Planning and estimating GCP product use using the Pricing Calculator
## 2.2 Planning and configuring compute resources. Considerations include:
- Selecting appropriate compute choices for a given workload (e.g., Compute Engine, Google Kubernetes Engine, App Engine, Cloud Run, Cloud Functions)

    - Qwiklabs
    - GCP Docs
      [Compute Engine](https://cloud.google.com/compute/docs/concepts)
      [GKE](https://cloud.google.com/kubernetes-engine/docs/concepts)
      [App Engine](https://cloud.google.com/appengine/docs)
      [Cloud Run](https://cloud.google.com/run/docs/concepts)
      [Cloud Functions](https://cloud.google.com/functions/docs/concepts)

- Using preemptible VMs and custom machine types as appropriate

    - Qwiklabs
    - GCP Docs
      - [Preempitble](https://cloud.google.com/compute/docs/instances/preemptible)
      - [Custom Machine Types](https://cloud.google.com/compute/docs/machine-types#custom_machine_types)

## 2.3 Planning and configuring data storage options. Considerations include:
- Product choice (e.g., Cloud SQL, BigQuery, Cloud Spanner, Cloud Bigtable)

    - Qwiklabs
      - [Cloud SQL]()
      - [Cloud Spanner]()
      - [Cloud Bigtable]()
      - [Cloud BigQuery]()
      - [Cloud Memorystore]()
      - [Cloud Firestore]()
      - [Cloud Filestore]()
      - [Cloud Storage for Firebase]()
    - GCP Docs
      - [Cloud SQL](ihttps://cloud.google.com/sql/docs/concepts)
      - [Cloud Spanner](https://cloud.google.com/spanner/docs/concepts)
      - [Cloud Bigtable](https://cloud.google.com/bigtable/docs/concepts)
      - [Cloud BigQuery](https://cloud.google.com/bigquery/docs/tutorials)
      - [Cloud Memorystore](ihttps://cloud.google.com/memorystore/docs/redis/concepts)
      - [Cloud Firestore](https://cloud.google.com/firestore/docs/concepts)
      - [Cloud Filestore](https://cloud.google.com/filestore/docs/concepts)
      Below is not part of Exam guide but quick view is good.
      - [Cloud Storage for Firebase](https://firebase.google.com/docs)

- Choosing storage options (e.g., Standard, Nearline, Coldline, Archive)

    - Qwiklabs
      - [Cloud Storage](https://cloud.google.com/storage/docs/concepts)
      - [Cloud Storage Standard](https://cloud.google.com/storage/docs/storage-classes#standard)
      - [Cloud Storage Nearline](https://cloud.google.com/storage/docs/storage-classes#nearline)
      - [Cloud Storage Coldline](https://cloud.google.com/storage/docs/storage-classes#coldline)
      - [Cloud Storage Archive](https://cloud.google.com/storage/docs/storage-classes#archive)
      - [Cloud Storage Additional/Legacy Classes](https://cloud.google.com/storage/docs/storage-classes#legacy)
    - GCP Docs
      - [Cloud Storage](https://cloud.google.com/storage/docs/concepts)
      - [Cloud Storage Standard](https://cloud.google.com/storage/docs/storage-classes#standard)
      - [Cloud Storage Nearline](https://cloud.google.com/storage/docs/storage-classes#nearline)
      - [Cloud Storage Coldline](https://cloud.google.com/storage/docs/storage-classes#coldline)
      - [Cloud Storage Archive](https://cloud.google.com/storage/docs/storage-classes#archive)
      - [Cloud Storage Additional/Legacy Classes](https://cloud.google.com/storage/docs/storage-classes#legacy)

## 2.4 Planning and configuring network resources. Tasks include:
- Differentiating load balancing options

    - Qwiklabs
    - GCP Docs
      - [Cloud Balancing Overview](https://cloud.google.com/load-balancing/docs/load-balancing-overview)
      - [Cloud Load Balancing](https://cloud.google.com/load-balancing)
      - [Choosing Load Balancer](https://cloud.google.com/load-balancing/docs/choosing-load-balancer)
      - [Summary of Load Balancing Options](https://cloud.google.com/load-balancing/docs/choosing-load-balancer#summary-of-google-cloud-load-balancers)
      - [L7 Internal HTTP(s) LB](https://cloud.google.com/load-balancing/docs/l7-internal)
      - [External HTTP(s) LB](https://cloud.google.com/load-balancing/docs/https)
      - [Internal TCP/UDP LB](https://cloud.google.com/load-balancing/docs/internal)
      - [External TCP/UDP Network LB](https://cloud.google.com/load-balancing/docs/network)
      - [SSL Proxy LB](https://cloud.google.com/load-balancing/docs/ssl)
      - [TCP Proxy LB](https://cloud.google.com/load-balancing/docs/tcp)

- Identifying resource locations in a network for availability

    - Qwiklabs
    - GCP Docs
      - [Creating VPC](https://cloud.google.com/vpc/docs/using-vpc#creating_networks)
      - [Working with Subnets](https://cloud.google.com/vpc/docs/using-vpc#subnet-rules)
      - [Modify Networks](https://cloud.google.com/vpc/docs/using-vpc#modifying_a_vpc_network)
      - [Create Firewall Rules](https://cloud.google.com/vpc/docs/using-firewalls#creating_firewall_rules)
      - [Using Routes](https://cloud.google.com/vpc/docs/using-routes)
      - [Network Tags](https://cloud.google.com/vpc/docs/add-remove-network-tags)
      - [Provision Shared VPC](https://cloud.google.com/vpc/docs/provisioning-shared-vpc)
      - [De-Provision SHared VPC](https://cloud.google.com/vpc/docs/deprovisioning-shared-vpc)
      - [VPC Network Peering](https://cloud.google.com/vpc/docs/using-vpc-peering)
      - [Create Instances with Multiple Network Interfaces](https://cloud.google.com/vpc/docs/create-use-multiple-interfaces)
      - [Reserve Static Internal IP](https://cloud.google.com/compute/docs/ip-addresses/reserve-static-internal-ip-address)
      - [Reserve Static External IP](https://cloud.google.com/compute/docs/ip-addresses/reserve-static-external-ip-address)
      - [Cloud VPN](https://cloud.google.com/network-connectivity/docs/vpn/concepts)
      - [Cloud Interconnect](https://cloud.google.com/network-connectivity/docs/interconnect/concepts)
        - Partner Interconnect
        - Dedicated Interconnect
      - [Cloud Router](https://cloud.google.com/network-connectivity/docs/router/concepts)

- Configuring Cloud DNS

    - Qwiklabs
    - GCP Docs
      - [Cloud DNS](https://cloud.google.com/dns/docs/concepts)
      - [DNS Security (DNSSEC)](https://cloud.google.com/dns/docs/dnssec-config)

# 3. Deploying and implementing a cloud solution

## 3.1 Deploying and implementing Compute Engine resources. Tasks include:
- Launching a compute instance using Cloud Console and Cloud SDK (gcloud) (e.g., assign disks, availability policy, SSH keys)

    - Qwiklabs
    - GCP Docs
      - [Compute Engine](https://cloud.google.com/compute/docs/concepts)

- Creating an autoscaled managed instance group using an instance template

    - Qwiklabs
    - GCP Docs
      - [Instance Template](https://cloud.google.com/compute/docs/instance-templates)
      - [Instance Group](https://cloud.google.com/compute/docs/instance-groups)
      - [Create Managed Instance Group](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances)

- Generating/uploading a custom SSH key for instances

    - Qwiklabs
    - GCP Docs
      - [SSH with Security keys](https://cloud.google.com/compute/docs/tutorials/ssh-with-sk)

- Configuring a VM for Stackdriver monitoring and logging
    - Qwiklabs
    - GCP Docs
- Assessing compute quotas and requesting increases
    - Qwiklabs
    - GCP Docs
- Installing the Stackdriver Agent for monitoring and logging
    - Qwiklabs
    - GCP Docs
      - [Operations (Formerly Stackdriver)](https://cloud.google.com/products/operations)

## 3.2 Deploying and implementing Google Kubernetes Engine resources. Tasks include:
- Deploying a Google Kubernetes Engine cluster

    - Qwiklabs
      - [Deploy K8s to GCP](https://google.qwiklabs.com/quests/116?utm_source=google&utm_medium=lp&utm_campaign=GKE)
      - [K8s Solutions](https://google.qwiklabs.com/quests/45?utm_source=google&utm_medium=lp&utm_campaign=GKE)
    - GCP Docs
      - [Create Zonal Cluster](https://cloud.google.com/kubernetes-engine/docs/how-to/creating-a-zonal-cluster)
      - [Create Regional CLuster](https://cloud.google.com/kubernetes-engine/docs/how-to/creating-a-regional-cluster)
      - [Create Private Cluster](https://cloud.google.com/kubernetes-engine/docs/how-to/private-clusters)
      - [Create Alpha Cluster](https://cloud.google.com/kubernetes-engine/docs/how-to/creating-an-alpha-cluster)
      - [Create Windows Server Node pool cluster](https://cloud.google.com/kubernetes-engine/docs/how-to/creating-a-cluster-windows)

- Deploying a container application to Google Kubernetes Engine using pods
    - Qwiklabs
    - GCP Docs
- Configuring Google Kubernetes Engine application monitoring and logging
    - Qwiklabs
    - GCP Docs

## 3.3 Deploying and implementing App Engine, Cloud Run, and Cloud Functions resources. Tasks include, where applicable:
- Deploying an application, updating scaling configuration, versions, and traffic splitting
    - Qwiklabs
    - GCP Docs
- Deploying an application that receives Google Cloud events (e.g., Cloud Pub/Sub events, Cloud Storage object change notification events)
    - Qwiklabs
    - GCP Docs

## 3.4 Deploying and implementing data solutions. Tasks include:
- Initializing data systems with products (e.g., Cloud SQL, Cloud Datastore, BigQuery, Cloud Spanner, Cloud Pub/Sub, Cloud Bigtable, Cloud Dataproc, Cloud Dataflow, Cloud Storage)
    - Qwiklabs
    - GCP Docs
- Loading data (e.g., command line upload, API transfer, import/export, load data from Cloud Storage, streaming data to Cloud Pub/Sub)
    - Qwiklabs
    - GCP Docs

## 3.5 Deploying and implementing networking resources. Tasks include:
- Creating a VPC with subnets (e.g., custom-mode VPC, shared VPC)
    - Qwiklabs
    - GCP Docs
- Launching a Compute Engine instance with custom network configuration (e.g., internal-only IP address, Google private access, static external and private IP address, network tags)
    - Qwiklabs
    - GCP Docs
- Creating ingress and egress firewall rules for a VPC (e.g., IP subnets, tags, service accounts)
    - Qwiklabs
    - GCP Docs
- Creating a VPN between a Google VPC and an external network using Cloud VPN
    - Qwiklabs
    - GCP Docs
- Creating a load balancer to distribute application network traffic to an application (e.g., Global HTTP(S) load balancer, Global SSL Proxy load balancer, Global TCP Proxy load balancer, regional network load balancer, regional internal load balancer)
    - Qwiklabs
    - GCP Docs

## 3.6 Deploying a solution using Cloud Marketplace. Tasks include:
- Browsing Cloud Marketplace catalog and viewing solution details
    - Qwiklabs
    - GCP Docs
- Deploying a Cloud Marketplace solution
    - Qwiklabs
    - GCP Docs

## 3.7 Deploying application infrastructure using Cloud Deployment Manager. Tasks include:
- Developing Deployment Manager templates
    - Qwiklabs
    - GCP Docs
- Launching a Deployment Manager template
    - Qwiklabs
    - GCP Docs

# 4. Ensuring successful operation of a cloud solution
## 4.1 Ensuring successful operation of a cloud solution
- Managing a single VM instance (e.g., start, stop, edit configuration, or delete an instance)

    - Qwiklabs
    - GCP Docs
      - [Start Stop Instance](https://cloud.google.com/compute/docs/instances/stop-start-instance)
      - [Suspend Resume](https://cloud.google.com/compute/docs/instances/suspend-resume-instance)
      - [Delete](https://cloud.google.com/compute/docs/instances/deleting-instance)
      - [Update Instance Properties](https://cloud.google.com/compute/docs/instances/update-instance-properties)

- SSH/RDP to the instance

    - Qwiklabs
    - GCP Docs
      - [Connect](https://cloud.google.com/compute/docs/instances/connecting-to-instance)
      - [Advance Connect](https://cloud.google.com/compute/docs/instances/connecting-advanced)

- Attaching a GPU to a new instance and installing CUDA libraries

    - Qwiklabs
    - GCP Docs
      - [Add GPU](https://cloud.google.com/compute/docs/gpus/add-gpus)
      - [Add Drivers](https://cloud.google.com/compute/docs/gpus/install-drivers-gpu)

- Viewing current running VM inventory (instance IDs, details)
    - Qwiklabs
    - GCP Docs
- Working with snapshots (e.g., create a snapshot from a VM, view snapshots, delete a snapshot)

    - Qwiklabs
    - GCP Docs
      - [Create Snapshot](https://cloud.google.com/compute/docs/disks/create-snapshots)
      - [Create Scheduled Snapshot](https://cloud.google.com/compute/docs/disks/scheduled-snapshots)
      - [Restore-Delete Snapshot](https://cloud.google.com/compute/docs/disks/restore-and-delete-snapshots)

- Working with images (e.g., create an image from a VM or a snapshot, view images, delete an image)

    - Qwiklabs
    - GCP Docs
      - [Create Image](https://cloud.google.com/compute/docs/machine-images/create-machine-images)
      - [Create InstanceFrom Image](https://cloud.google.com/compute/docs/machine-images/create-instance-from-machine-image)
      - [View Source Image](https://cloud.google.com/compute/docs/instances/view-vm-image)
      - [Delete Custom Image](https://cloud.google.com/compute/docs/images/create-delete-deprecate-private-images)

- Working with instance groups (e.g., set autoscaling parameters, assign instance template, create an instance template, remove instance group)

    - Qwiklabs
    - GCP Docs
      - [Instance Group](https://cloud.google.com/compute/docs/instance-groups)
      - [Create Managed Instance Group](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances)

- Working with management interfaces (e.g., Cloud Console, Cloud Shell, GCloud SDK)
    - Qwiklabs
    - GCP Docs
## 4.2 Managing Google Kubernetes Engine resources. Tasks include:
- Viewing current running cluster inventory (nodes, pods, services)
    - Qwiklabs
    - GCP Docs
- Browsing the container image repository and viewing container image details
    - Qwiklabs
    - GCP Docs
- Working with node pools (e.g., add, edit, or remove a node pool)
    - Qwiklabs
    - GCP Docs
- Working with pods (e.g., add, edit, or remove pods)
    - Qwiklabs
    - GCP Docs
- Working with services (e.g., add, edit, or remove a service)
    - Qwiklabs
    - GCP Docs
- Working with stateful applications (e.g. persistent volumes, stateful sets)
    - Qwiklabs
    - GCP Docs
- Working with management interfaces (e.g., Cloud Console, Cloud Shell, Cloud SDK)
    - Qwiklabs
    - GCP Docs
## 4.3 Managing App Engine and Cloud Run resources. Tasks include:
- Adjusting application traffic splitting parameters
    - Qwiklabs
    - GCP Docs
- Setting scaling parameters for autoscaling instances
    - Qwiklabs
    - GCP Docs
- Working with management interfaces (e.g., Cloud Console, Cloud Shell, Cloud SDK)
    - Qwiklabs
    - GCP Docs

## 4.4 Managing storage and database solutions. Tasks include:
- Moving objects between Cloud Storage buckets
    - Qwiklabs
    - GCP Docs
- Converting Cloud Storage buckets between storage classes
    - Qwiklabs
    - GCP Docs
- Setting object life cycle management policies for Cloud Storage buckets
    - Qwiklabs
    - GCP Docs
- Executing queries to retrieve data from data instances (e.g., Cloud SQL, BigQuery, Cloud Spanner, Cloud Datastore, Cloud Bigtable)
    - Qwiklabs
    - GCP Docs
- Estimating costs of a BigQuery query
    - Qwiklabs
    - GCP Docs
- Backing up and restoring data instances (e.g., Cloud SQL, Cloud Datastore)
    - Qwiklabs
    - GCP Docs
- Reviewing job status in Cloud Dataproc, Cloud Dataflow, or BigQuery
    - Qwiklabs
    - GCP Docs
- Working with management interfaces (e.g., Cloud Console, Cloud Shell, Cloud SDK)
    - Qwiklabs
    - GCP Docs
## 4.5 Managing networking resources. Tasks include:
- Adding a subnet to an existing VPC
    - Qwiklabs
    - GCP Docs
      - [Working with Subnets](https://cloud.google.com/vpc/docs/using-vpc#subnet-rules)
- Expanding a subnet to have more IP addresses
    - Qwiklabs
    - GCP Docs
      - [Working with Subnets](https://cloud.google.com/vpc/docs/using-vpc#subnet-rules)
- Reserving static external or internal IP addresses
    - Qwiklabs
    - GCP Docs
      - [Reserve Static Internal IP](https://cloud.google.com/compute/docs/ip-addresses/reserve-static-internal-ip-address)
      - [Reserve Static External IP](https://cloud.google.com/compute/docs/ip-addresses/reserve-static-external-ip-address)
- Working with management interfaces (e.g., Cloud Console, Cloud Shell, Cloud SDK)
    - Qwiklabs
    - GCP Docs
## 4.6 Monitoring and logging. Tasks include:
- Creating Stackdriver alerts based on resource metrics
    - Qwiklabs
    - GCP Docs
- Creating Stackdriver custom metrics
    - Qwiklabs
    - GCP Docs
- Configuring log sinks to export logs to external systems (e.g., on-premises or BigQuery)
    - Qwiklabs
    - GCP Docs
- Viewing and filtering logs in Stackdriver
    - Qwiklabs
    - GCP Docs
- Viewing specific log message details in Stackdriver
    - Qwiklabs
    - GCP Docs
- Using cloud diagnostics to research an application issue (e.g., viewing Cloud Trace data, using Cloud Debug to view an application point-in-time)
    - Qwiklabs
    - GCP Docs
- Viewing Google Cloud Platform status
    - Qwiklabs
    - GCP Docs
- Working with management interfaces (e.g., Cloud Console, Cloud Shell, Cloud SDK)
    - Qwiklabs
    - GCP Docs

# 5 Configuring access and security
- Qwiklabs
- GCP Docs
  - [Security Design](https://cloud.google.com/security/infrastructure/design)
## 5.1 Managing identity and access management (IAM). Tasks include:
- Viewing IAM role assignments
    - Qwiklabs
    - GCP Docs
- Assigning IAM roles to accounts or Google Groups
    - Qwiklabs
    - GCP Docs
- Defining custom IAM roles
    - Qwiklabs
    - GCP Docs
## 5.2 Managing service accounts. Tasks include:
- Managing service accounts with limited privileges
    - Qwiklabs
    - GCP Docs
- Assigning a service account to VM instances
    - Qwiklabs
    - GCP Docs
- Granting access to a service account in another project
    - Qwiklabs
    - GCP Docs 
## 5.3 Viewing audit logs for project and managed services.

# CLI Code Errors

[Code Errors](https://cloud.google.com/resource-manager/docs/core_errors)
