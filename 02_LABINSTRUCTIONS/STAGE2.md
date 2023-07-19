# Tiered Storage with S3 File Gateway - Create an S3 bucket with storage tiering

![Architecture](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE2.png)

- Stage 1: Create & Activate the storage gateway
- Stage 2: Create an S3 bucket with storage tiering <= `YOU ARE HERE`
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

# Create the first bucket
Head to the S3 dashboard: [https://s3.console.aws.amazon.com/s3/buckets](https://s3.console.aws.amazon.com/s3/buckets)

Click <kbd>Create bucket</kbd>

Pick a `Bucket Name`, I'll use `3-file-gateway-bucket-7733` (The bucket name must be globally unique so you will have to choose a different name)

Set the region to `us-east-1` or whichever region you’re using

Leave everything else as default and click <kbd>Create bucket</kbd>

# Storage Tiering

Select your bucket and go to `management`

Under `Lifecycle rules` click <kbd>Create lifecycle rule</kbd>  

Pick a `Lifecycle rule name`, I'll use `infrequent-access-rule`

Set the `Prefix` to `/`

Under `Lifecycle rule actions` choose `Move current versions of objects between storage classes`

Under `Choose storage class transitions
D` select `Standard-IA` 

Change `Days after object creation` to `30`

Leave everything else as default and click <kbd>Create Rule</kbd>
