# Compute Instances

1. Not managed by GCP.
2. Works on vCPU (which is Hyperthread model).
3. Runs Linux or Windows image which GCP provides or a private Custom images.
4. Use Instance Group to manage multiple instances together, configure autoscaling.
5. Attache Persistent disk - SSD with default AES 256 encryption or HDD with default AES 128 encryption. Has a default boot persistent disk
6. Can also run Docker containers on [Container-Optimized](https://cloud.google.com/container-optimized-os/docs) OS image.
7. Each VM belongs to one VPC and instances in same network communicate through Local area network.
8. The default TZ of VM is UTC.



### CLI Commands

#### Configure Region and Zone

> ``gcloud config set compute/region us-east1``
>
> ``gcloud config set compute/zone us-east1-a``

#### List and describe instances

> ``gcloud compute instances list``
>
> ``gcloud compute instances describe INSTANCE-1``

#### Delete instance:
> ``gcloud compute instances delete INSTANCE-1``

#### Get iAM policy for Instance

> ``gcloud compute instances get-iam-policy INSTANCE-1`` 

#### Add and Revoke iAM policy for Instance

>``gcloud compute instances remove-iam-policy-binding INSTANCE-1 --member=user:test-user@gmail.com --role=role/viewer``
>> --member should be of the form ``user|group|serviceAccount:email or domain:domain``
>>>
>> Examples: ``user:test-user@gmail.com, group:admins@example.com, serviceAccount:test123@example.domain.com, or domain:example.domain.com``

#### Help documents
> ``gcloud compute instances --help``
