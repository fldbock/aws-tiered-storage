# Tiered Storage with S3 File Gateway

In this demo, you will configure a s3 file gateway, allowing on premises servers to use it as an nfs server, with the added benefit of saving costs using s3 for storage tiering

The demo consists of 5 stages, each implementing additional components of the architecture
- Stage 1: Create & Active the storage gateway
- Stage 2: Create the S3 buckets, storage tiering and cross region replication
- Stage 3: Create a file share
- Stage 4: Mount the storage gateway on your local file system
- Stage 5: Cleanup

![Architecture](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE4.png)

## 1-Click Installs (DO THIS FIRST)

Make sure you are logged into AWS and in `us-east-1`

- [VPC](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?templateURL=https://s3.us-east-1.amazonaws.com/flortechconsultancy-cloudformation-templates/aws-tiered-storage/aws-tiered-storage-base-template.yaml&stackName=AWSTieredStorageStack)

## Instructions

- [Stage1](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE1.md)
- [Stage2](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE2.md)
- [Stage3](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE3.md)
- [Stage4](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE4.md)
- [Stage5](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE5.md)

## Architecture Diagrams

- [Stage1](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE1.png)
- [Stage2](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE2.png)
- [Stage3](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE3.png)
- [Stage4](https://github.com/fldbock/aws-tiered-storage/blob/main/02_LABINSTRUCTIONS/STAGE4.png)



