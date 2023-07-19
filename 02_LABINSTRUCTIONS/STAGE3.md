# Tiered Storage with S3 File Gateway - Create a file share

![Architecture](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE3.png)

- Stage 1: Create & Activate the storage gateway
- Stage 2: Create an S3 bucket with storage tiering
- Stage 3: Create a file share <= `YOU ARE HERE`
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

# Create a file share

Head to the Storage Gateway dashboard: [https://console.aws.amazon.com/storagegateway/home](https://console.aws.amazon.com/storagegateway/home)

In the menu select `File shares` and click <kbd>Create file share</kbd>

Under `Gateway` select the gateway we just created

Select `NFS`

Select the S3 bucket we created previously

Click <kbd>Create file share</kbd>

Wait for the Status of the file share to be `available` before moving on