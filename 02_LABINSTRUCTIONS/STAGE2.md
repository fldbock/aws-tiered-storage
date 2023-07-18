# Tiered Storage with S3 File Gateway - Create the S3 buckets, storage tiering and cross region replication

- Stage 1: Create & Active the storage gateway 
- Stage 2: Create the S3 buckets, storage tiering and cross region replication <= `YOU ARE HERE`
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

# Create the first bucket
Head to the S3 dashboard: [https://s3.console.aws.amazon.com/s3/buckets](https:>

Click on <kbd>Create bucket</kbd>

For **Bucket Name**, I will use “s3-file-gateway-bucket-7733”. The bucket name must be globally unique so you will have to choose a different name.

Set the region to `us-east-1` or whichever region you’re using.

Leave everything else as default and click <kbd>Create bucket</kbd>

# Storage Tiering

Click on your bucket name and go to "management".

Click on "Create lifecycle rule" under "Lifecycle rules".

Set the Lifecycle rule name to `infrequent-access-rule`

Set the Prefix to `/`

Under "Lifecycle rule actions" choose `Move current versions of objects between storage classes`

Select `Standard-IA` under "Choose storage class transitions
D"

Change "Days after object creation" to `30`

Leave everything else as default and click <kbd>Create Rule</kbd>
