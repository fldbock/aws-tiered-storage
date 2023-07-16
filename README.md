# Tiered Storage with S3 File Gateway

## Case Study

Situation:
A company uses a lot of storage on it’s nfs server on the on premises
network most of which it hardly ever accesses. Surely we can use cloud
computing to save some cost here?

Requirements:
The documents need to be accessible in the usual way with minimal
latency. The company also wonders if we could make the storage more
resilient in case of disaster.

Solution:

We are going to set up a s3 file gateway to implement tiered storage and cross region replication for disaster recovery.

The demo consists of 4 stages, each implementing additional components of the architecture.
- Stage 1: Create & Active the storage gateway
- Stage 2: Create the S3 buckets, storage tiering and cross region replication
- Stage 3: Create a bucket share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup
- 
## 1-Click Installs (DO THIS FIRST)

Make sure you are logged into AWS and in `us-east-1`
## Instructions

- Stage 1: Create & Active the storage gateway
- Stage 2: Create the S3 buckets, storage tiering and cross region replication
- Stage 3: Create a bucket share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

