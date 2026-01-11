## 1. Subnets

Public Subnet:
- Internet accessible
- Connected to IGW

Private Subnet:
- No direct internet access

Terraform handles dependencies automatically.

---

## 2. VPC Basics
A logically isolated network.

Defined by:
- CIDR block
- Route tables
- Subnets

---

## 3. Terraform State
terraform.tfstate tracks infra.

Best practice:
Remote state using:
- S3 (storage)
- DynamoDB (locking)

---

## 4. Terraform File Structure
main.tf → main config
network.tf → VPC, subnets
compute.tf → EC2, security groups

---

## 5. IP Types
Private IP → internal
Public IP → internet
Elastic IP → static public IP

---

## 6. EC2 Creation
Requires AMI.
AMI defines OS.

---

## 7. Variables

Input variables → customization
Output variables → display info
Local variables → limited scope