# Tiered Storage with S3 File Gateway - Cleanup

- Stage 1: Create & Activate the storage gateway
- Stage 2: Create an S3 bucket with storage tiering
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup <= `YOU ARE HERE`

# Delete S3 Bucket

Head to the S3 dashboard: [https://s3.console.aws.amazon.com/s3/buckets](https://s3.console.aws.amazon.com/s3/buckets)

Select your s3 bucket and click on <kbd>Empty</kbd>

Type `permanently delete` to confirm you want to empty your bucket

Click <kbd>Exit</kbd>

Select your s3 bucket again and click on <kbd>Delete</kbd>

Type the name of your s3 bucket to confirm you want to delete your bucket

# Delete the Storage Gateway

Head to the Storage Gateway dashboard: [https://console.aws.amazon.com/storagegateway/home](https://console.aws.amazon.com/storagegateway/home)

Click on <kbd>File shares</kbd> in the menu, select your file share and click <kbd>Actions</kbd> followed by <kbd>Delete file share</kbd> 

Type `delete` to confirm you want to delete your file share

Click on <kbd>Gateways</kbd> in the menu, select your s3 file gateway and click <kbd>Actions</kbd> followed by <kbd>Delete gateway</kbd> 

Type `delete` to confirm you want to delete your file share

# Delete the storage gateway instance

Head to the EC2 dashboard: [https://console.aws.amazon.com/ec2/home](https://console.aws.amazon.com/ec2/home)
 
Go to `Instances` in the side menu, select the storagegateway-wizard instance and click <kbd>Inner State</kbd> followed by <kbd>Terminate instance</kbd>, click <kbd>Terminate</kbd> again to confirm you want to terminate the instance

Go to `Security Groups` in the side menu and delete the storagegateway-wizard security group. (You can only do this when the storagegatway-wizard ec2 instance is terminated)

# Delete the Cloudformation stack

Head to the cloudformation dashboard: [https://console.aws.amazon.com/cloudformation/home](https://console.aws.amazon.com/cloudformation/home)

Click on your one-click deployment stack and delete it