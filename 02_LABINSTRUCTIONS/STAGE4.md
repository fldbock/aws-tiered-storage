# Tiered Storage with S3 File Gateway - Mount the storage gateway on your local file system

- Stage 1: Create & Active the storage gateway 
- Stage 2: Create the S3 buckets, storage tiering and cross region replication 
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system <= `YOU ARE HERE`
- Stage 5: Cleanup

# SSH into on premises server

Head to the EC2 dashboard: [https://console.aws.amazon.com/ec2/home](https://console.aws.amazon.com/ec2/home)
 
Go to "Instances", select the OnpremServer instance and click <kbd>Connect</kbd>

Select "Session manager" and click <kbd>Connect</kbd>

# Mount onto storage gateway

Type "bash" and "cd". 

Type "sudo yum install nfs-utils" to install the NFS client packages.

Type "mkdir shared-files" 

Type "sudo mount -t nfs -o nolock,hard 10.0.0.234:/s3-file-gateway-bucket-1155 shared-files"


# Create files

Type "cd shared-files/"

Let's create a test folder and some test files.

Type "touch testfile1.txt" "mkdir testfolder" "touch testfolder/testfile2.txt"


# Check if it worked in S3

Head to the S3 dashboard: [https://s3.console.aws.amazon.com/s3/buckets](https://s3.console.aws.amazon.com/s3/buckets)

Click on your bucket name and got "management".

Now you can verify that the files and folders are in your bucket.

Congratulations!