# Compute Instances

1. Not managed by GCP.
2. Works on vCPU (which is Hyperthread model).
3. Runs Linux or Windows image which GCP provides or a private Custom images.
4. Use Instance Group to manage multiple instances together, configure autoscaling.
5. Attache Persistent disk - SSD with default AES 256 encryption or HDD with default AES 128 encryption. Has a default boot persistent disk
6. Can also run Docker containers on [Container-Optimized](https://cloud.google.com/container-optimized-os/docs) OS image.
7. Each VM belongs to one VPC and instances in same network communicate through Local area network.
8. The default TZ of VM is UTC.

## Machine Types

### Classification

| Type              | Names             | Supports Custom   | Supports Local SSD        |
| :---              |    :----         | :----:            |          :----           |
| General Purpose   | E2, N2, N2D, N1   | Yes               | Except E2                 |
| Compute Optimized | C2                | No                | Yes                       |
| Memory Optimized  | M1, M2            | No                | Ultramem: No. Megamem: Yes|
| Shared Core       | E2, N1, f1, g1    | No                |                           |

### vCPU to memory Ratio

| Type        | vCPU-to-Memory Ratio | Exception  |
| :---        |    :----:            | :----:     |
| Standard    | 1:4                  | N1: 1:3.75 |
| Highmem     | 1:8                  | N1: 1:6.50 |
| Highcpu     | 1:1                  | N1: 1:0.90 |

## Migration of VMs

During migration, from one host to another, it moves the complete instance state from the source to the destination in a way that is transparent to the guest OS and anyone communicating with it
All VM properties and attributes remain unchanged, including internal and external IP addresses, instance metadata, block storage data and volumes, OS and application state, network settings, network connections, and so on.

Read the [Live Migration Document](https://cloud.google.com/compute/docs/instances/live-migration)

## Preemptible Vms

Compute Engine doesn't charge you for instances if they are preempted in the first minute after they start running

## Shielded Vms

[Documentation](https://cloud.google.com/security/shielded-cloud/shielded-vm)

## Sole Tenant Nodes

Sole-tenancy lets you have exclusive access to a sole-tenant node, which is a physical Compute Engine server that is dedicated to hosting only your project's VMs.

[Documentation](https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes)

## CLI Commands

#### Configure Region and Zone

> ``gcloud config set compute/region us-east1``
>
> ``gcloud config set compute/zone us-east1-a``
>
> ``gcloud compute instances create example-instance --zone us-central1-f``
> ``gcloud compute instances create example-instance --zone us-central1-f --metadata startup-script="apt-get install apache"``
> ``gcloud compute instances create example-instance --zone us-central1-f --metadata-from-file startup-script="/opt/scripts/startup.sh""``

#### List, describe and filter instances

> ``gcloud compute instances list``
>
> ``gcloud compute instances describe INSTANCE-1``
> ``gcloud compute instances list --filter="zone:(us-central1-a)"``
> ``gcloud compute instances list --filter="name ~ .*INSTANCE.*"``

#### Delete instance:
> ``gcloud compute instances delete INSTANCE-1``

#### Reboot an instance:
> ``glcoud compute instances reset INSTANCE-1``

#### Connect and SCP to instance
> ``gcloud compute ssh INSTANCE-1 --zone us-central1-a``
> ``gcloud compute scp ~/file-1 INSTANCE-1:~/remote-destination --zone us-central1-a``

#### Get iAM policy for Instance

> ``gcloud compute instances get-iam-policy INSTANCE-1`` 

#### Add and Revoke iAM policy for Instance

>``gcloud compute instances remove-iam-policy-binding INSTANCE-1 --member=user:test-user@gmail.com --role=role/viewer``
>> --member should be of the form ``user|group|serviceAccount:email or domain:domain``
>>>
>> Examples: ``user:test-user@gmail.com, group:admins@example.com, serviceAccount:test123@example.domain.com, or domain:example.domain.com``

#### Working with Disks

Read or manage(create, delete) one or more persistent disks

> ``gcloud comute disks list``
>
> ``gcloud compute disks create my-disk-1 my-disk-2 --zone us-central1-a``
>
> ``gcloud compute disks create my-disk-1 --source-disk=disk --zone us-central1-a``
>
> ``gcloud compute disks create my-disk-1 --source-snapshot=snapshot --zone us-central1-a``
>
> ``gcloud compute disks delete my-disk-1 --zone us-central1-a``
>

#### Working with Images

Read or manage(create, delete) one or more images 

> ``gcloud compute images list`` 
>
> ``gcloud compute images create my-image --source-image=source-image --source-image-project=source-project`` 
>
> ``gcloud compute images create my-image --source-image-family=source-image-family --source-image-project=source-project`` 
>
> ``gcloud compute images create my-image --source-snapshot=source-snapshot`` 
>
> ``glcoud compute images delete my-image1 my-image2 --zone=us-east1-a --region=us-east1``

#### Working with Instance Templates

Read or manage(create, delete) one or more images 

> ``gcloud compute instance-templates list`` 
>
> ``gcloud compute instance-templates create instance-template-1`` 
>
> ``gcloud compute instance-templates create instance-template-1 --source-instance=instance1`` 
>
> ``gcloud compute instance-templates describe instance-template-1`` 
>
> ``gcloud compute instance-templates delete instance-template-1`` 

#### Working with Instance Groups

Read or manage(create, delete) one or more images 

> ``gcloud compute instance-groups managed list`` 
>
> ``gcloud compute instance-groups unmanaged list`` 
>
> ``gcloud compute instance-groups managed list-instances`` 
>
> ``gcloud compute instance-groups unmanaged list-instances`` 
>
> ``gcloud compute instance-groups managed create instance-group-1 --template=instance-template-1 --size=2`` 
>
> ``gcloud compute instance-groups managed create-instance <instance-group> --instance=instance-1`` 
>
> ``gcloud compute instance-groups managed describe instance-group-1`` 
>
> ``gcloud compute instance-groups managed describe --zone us-central1-a`` 
>
> ``gcloud compute instance-groups managed delete instance-group-1`` 

#### Help documents
> ``gcloud compute --help``

## Resources

### Qwiklabs

#### Labs
1. [Hosting a Web App on Google Cloud Using Compute Engine](https://www.qwiklabs.com/focuses/11952?catalog_rank=%7B%22rank%22%3A3%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379800)
2. [Setting up a Minecraft Server on Google Compute Engine](https://www.qwiklabs.com/focuses/1852?catalog_rank=%7B%22rank%22%3A4%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379800)
3. [Creating Custom Base Images for Compute Engine with Jenkins and Packer](https://www.qwiklabs.com/focuses/4167?catalog_rank=%7B%22rank%22%3A8%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379800)
4. [Deploy a Compute Instance with a Remote Startup Script](https://www.qwiklabs.com/focuses/1735?catalog_rank=%7B%22rank%22%3A5%2C%22num_filters%22%3A4%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379928)
5. [Autoscaling an Instance Group with Custom Cloud Monitoring Metrics](https://www.qwiklabs.com/focuses/611?catalog_rank=%7B%22rank%22%3A6%2C%22num_filters%22%3A4%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379928)
6. [HTTP Load Balancer](https://www.qwiklabs.com/focuses/699?catalog_rank=%7B%22rank%22%3A7%2C%22num_filters%22%3A4%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379928)
7. [Creating Cross-region Load Balancing](https://www.qwiklabs.com/focuses/642?catalog_rank=%7B%22rank%22%3A12%2C%22num_filters%22%3A4%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=7379938)

#### Quests
1. [Exploring APIs](https://www.qwiklabs.com/quests/54?catalog_rank=%7B%22rank%22%3A1%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379955)
2. [VM Migration](https://www.qwiklabs.com/quests/87?catalog_rank=%7B%22rank%22%3A3%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379955)
3. [Google Cloud Essentials](https://www.qwiklabs.com/quests/23?catalog_rank=%7B%22rank%22%3A6%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379955)
4. [Cloud Development](https://www.qwiklabs.com/quests/67?catalog_rank=%7B%22rank%22%3A13%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379967)
5. [Understanding Your Google Cloud Costs](https://www.qwiklabs.com/quests/90?catalog_rank=%7B%22rank%22%3A18%2C%22num_filters%22%3A2%2C%22has_search%22%3Atrue%7D&search_id=7379967)

### YouTube

1. [What is Compute Engine](https://youtu.be/KBeyQHoAcrQ)
2. [Introduction to Virtual Machines](https://youtu.be/3aNDcgoJ-_8)
3. [Best Practices for Managing Compute Engine VM Instances](https://youtu.be/ZJNY7VAKYzw)
