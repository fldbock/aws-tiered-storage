# Tiered Storage with S3 File Gateway - Create & Active the storage gateway

- Stage 1: Create & Active the storage gateway <= `YOU ARE HERE`
- Stage 2: Create the S3 buckets, storage tiering and cross region replication
- Stage 3: Create a bucket share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

# Set up your Amazon S3 File Gateway
Head to the Storage Gateway dashboard: [https://console.aws.amazon.com/storagegateway/home](https:>

Click on "Create gateway"

Set "Gateway name" to `s3-file-gateway`

Change the Gateway time zone to your current time zone.

Set "Host platform" to `Amazon EC2`

Keep "Use default settings" selected

Select `onprem-vpc`

Select `sn-onprem-vpc-public`

Select a key pair.

Click <kbd>Launch instance</kbd> and wait until the EC2 instance is launched.

Click <kbd>Next</kbd>

# Connect your Amazon S3 File Gateway to AWS

Leave "IP address" as the connection option

The public IP adress should have been automatically pre filled.

Under Service endpoint, leave "Publicly accessible" selected.

Click <kbd>Next</kbd>

# Review and activate

Review to make sure everything is filled in correctly.

Click <kbd>Activate gateway </kbd>

# Configure your Amazon S3 File Gateway

Wait until the "Configure cache storage" is loaded.

Select "Cache".

