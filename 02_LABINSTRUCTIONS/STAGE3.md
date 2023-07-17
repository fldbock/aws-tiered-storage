# Tiered Storage with S3 File Gateway - Create the S3 buckets, storage tiering and cross region replication

- Stage 1: Create & Active the storage gateway 
- Stage 2: Create the S3 buckets, storage tiering and cross region replication 
- Stage 3: Create a file share <= `YOU ARE HERE`
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

# Creat a file share

Head to the Storage Gateway dashboard: [https://console.aws.amazon.com/storagegateway/home](https:>

In the menu select "File shares" and click "Create file share"

Under "Gateway" select the gateway we just created.

Select "NFS".

Select the S3 bucket we created previously.

Click <kbd>Create file share</kbd>