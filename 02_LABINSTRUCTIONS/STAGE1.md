# Tiered Storage with S3 File Gateway - Create & Activate the storage gateway

![Architecture](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE1.png)

- Stage 1: Create & Activate the storage gateway <= `YOU ARE HERE`
- Stage 2: Create an S3 bucket with storage tiering
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

# Create the S3 File Gateway
Head to the Storage Gateway dashboard: [https://console.aws.amazon.com/storagegateway/home](https://console.aws.amazon.com/storagegateway/home)

Click `Create gateway`

Pick a `Gateway name`, I'll use `s3-file-gateway`

Under `Gateway time zone`, select your current time zone

Set `Host platform` to `Amazon EC2`

Keep `Use default settings` selected

Under `VPC` select `onprem-vpc`

Under `Subnets` select `sn-onprem-vpc-public`

Select a key pair

Click <kbd>Launch instance</kbd> and wait until the EC2 instance is launched, then click <kbd>Next</kbd>

# Connect the S3 File Gateway to AWS

Leave `IP address` as the connection option

The public IP adress should have been automatically pre filled.

Under `Service endpoint`, leave `Publicly accessible` selected.

Click <kbd>Next</kbd>

# Review and activate

Review to make sure everything is filled in correctly.

Click <kbd>Activate gateway</kbd>

# Configure the S3 File Gateway

Wait until the `Configure cache storage` is loaded, then select `Cache`.

Under `CloudWatch alarms` select `No alarm`

Click <kbd>Configure</kbd>
