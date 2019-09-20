# Services Overview

AWS comprises of several services that provide hopefully reliable
and secure cloud platform. Provided services built upon Virtual Private Cloud.

## VPC Service
VPC is basically servers connected to networks with specific configuration
and region. It automatically configured to be distributed into several
data center in an area, known as Availability Zone (AZ). It is also provide
multi-region instance, known as Region. Beside AZ and Region, some data storage
service amazon provides (S3 and CloudFront) need a high availability
and low latency therefore, need to be distributed near the target audience area.
This distribution known as Edge Location.

It also provide scalability horizontally or vertically. Horizontally, AWS enable
customer to create & destroy instances in minutes and even scheduling or listening
to trigger. Later to be learned. Vertically, it can upgrade each instance CPU
or memory quantity.

VPC enable network configuration among the VPC instances and to the external
network.

TODO: Network and security

## Elastic Cloud Compute (EC2)
Elastic compute is server resource, much like processor and memory package.
It is scalable in term of hardware resource type (freq & memory size) and in
the number of clone.

## Elastic Block Storage (EBS)
EBS is persistent storage resource, physically SSD and harddrive. It is scalable
on the fly, may be increased in size or performance (e.g. switching to SSD).
To connect with EC2, must be under the same availability zone (AZ), like `as-southeast-1b`.

## Simple Storage Service (S3)
S3 is a public-facing storage that host static files. It highly use cache
and duplication, empowered by Edge Locations to be accessible with low latency.

## Elastic Load Balancer (ELB)
Provide two kind of load balancer: classic and application. Application LB
has all classic has with additional features, such as health check, log refinement,
CloudWatch metric, additional supported protocol. We focused on Application LB.

Redirection is configured using domain, port, URL path, IP address, etc.
The balancing happened when the health check (of specific URL we registered)
return non HTTP 200.
