# Tiered Storage with S3 File Gateway - Mount the storage gateway on your local file system

![Architecture](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE4.png)

- Stage 1: Create & Activate the storage gateway
- Stage 2: Create an S3 bucket with storage tiering
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system <= `YOU ARE HERE`
- Stage 5: Cleanup

# Session manager

Head to the EC2 dashboard: [https://console.aws.amazon.com/ec2/home](https://console.aws.amazon.com/ec2/home)
 
Go to `Instances`, select the OnpremServer instance and click <kbd>Connect</kbd>

Select `Session manager` and click <kbd>Connect</kbd>

# Mount onto storage gateway

Type `sudo bash` and press enter
Type `cd` and press enter

First we need to install the amazon EFS utilities to allow the instance to connect to EFS. EFS is based on NFS which is standard but the EFS tooling makes things easier.

```
sudo yum install nfs-utils
```

Next we need to create a new folder where we will mount the storage gateway on.
You can find the private ip address of your storage gateway instance either by clicking on your storage gateway instance in the EC2 service console or by clicking on your storage gateway in the Storage Gateway service console.
```
mkdir shared-files
sudo mount -t nfs -o nolock,hard IPSTORAGEGATEWAYINSTANCE:/S3BUCKETNAME shared-files
```

# Create files

Let's create a test folder and some test files

```
cd shared-files/
touch testfile1.txt && mkdir testfolder && touch testfolder/testfile2.txt
```

# Check if it worked in S3

Head to the S3 dashboard: [https://s3.console.aws.amazon.com/s3/buckets](https://s3.console.aws.amazon.com/s3/buckets)

Click on your bucket name and go to `management`

Now you can verify that the files and folders are in your bucket (it can take a few minutes)

Congratulations! At this point you have a working storage gateway with storage tiering, which will save your company money if you have files that aren't frequently accessed, and you can't mount the storage gateway as an nfs file server on your on premises hosts.
In the next stage we will clear up all of the services that we used.