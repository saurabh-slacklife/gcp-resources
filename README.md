# Google Cloud Platform Offerings

# Table of Contents

1. [Compute](#compute)
2. [Network](#network) #WIP
3. [Storage](#storage) #TODO
4. [Database](#database) #TODO
4. [Big data](#big-data) #TODO
5. [Machine Learning](#machine-learning) #TODO

## Compute

GCP offers [Compute](./compute/Compute.md) options from IaaS to Serverless. The Virtual Machines(VM) works on Hyper Thread model with each Virtual CPU(vCPU) corresponds to one Hyper Thread.
The VMs are located in a Zone.

## Network

GCP offers network connectivity through the Virtual Private Cloud (VPC) to Load balance the resources, create DNS records or connect on-premises/existing network to GCP network.


## Storage

The Storage Services includes - Cloud Storage, Persistent Disk on Compute Engine, fully managed NFS Filestore.

## Database

DCP Offers both SQL and NoSql Databases

| Name | Type | Transactional | Scalability | Data Distribution |
| :--- | :----: | :----: | :----: | :----: |
| Cloud SQL | SQL | Transactional | Region (#CHECK) | Zonal |
| Cloud Spanner | SQL | Transactional | Horizontal Scaling | Regional or Global |
| Cloud Big Query | Warehouse | Transactional | Scalable | |
| Cloud Bigtable | NoSql Column based on HBase | No | Scalable | Regional or Global |
| Cloud Firestore | NoSql Document | Transactional | Scalable | Regional or Global | 
| Cloud Memorystore | In-memory Redis or Memcached | No | Scalable | Zonal |

## Big data

## Machine Learning



