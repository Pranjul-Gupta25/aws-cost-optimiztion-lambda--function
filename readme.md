# AWS Lambda: EC2 Volume and Snapshot Cleanup

This AWS Lambda function helps clean up unused EBS volumes and associated snapshots. It performs the following operations:

1. Lists all running EC2 instances.
2. Checks all EBS volumes.
3. Deletes volumes that are not attached to any running EC2 instance.
4. Checks snapshots and deletes those whose associated volume is unused and has been deleted.

---

## ✅ Features

- Identifies **unattached EBS volumes**.
- Ensures **volumes in use by running instances are not deleted**.
- Deletes **snapshots** associated with unused volumes.
- Logs all actions in **CloudWatch Logs**.

---

## 🧪 Usage

### 1. **Deploy the Lambda Function**

- Create a Lambda function using Python 3.9+.
- Copy the code into a file named `lambda_function.py`.
- Attach an IAM role with the necessary permissions (see below).

### 2. **IAM Role Permissions**

Ensure your Lambda function has an IAM role with at least the following permissions:

AWSLambdaBasic ExecutionRole-
cost-optimization-ebs 
ec-2permission-cost 
ec2-delete-volume 


created these policy by own 
