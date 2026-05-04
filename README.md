given task 
Create VPC with:
* 2 public + 2 private subnets (multi-AZ)
Internet Gateway + NAT Gateway
* Deploy ALB (public)
Route HTTP traffic to backend
* Create Launch Template + Auto Scaling Group
Instances in private subnet
* Min: 2, Max: 5
Install Nginx
Configure Security Groups
* Allow HTTP → ALB
* Allow ALB → EC2 only
Create RDS (MySQL/Postgres)
* Private subnet
* Accessible only from EC2
Create S3 bucket
* Enable versioning


Use modules (VPC, EC2, RDS)
Use variables (region, instance type, DB name)
Support dev & prod environments
Conditional logic:
* dev → 1 instance
* prod → autoscaling
Add lifecycle rule
* Prevent DB deletion



ec2 instance  <img width="959" height="437" alt="{BCB4620E-95AF-47A8-AD00-23D89365A46C}" src="https://github.com/user-attachments/assets/4d7ae4d6-4c4b-4d09-b638-e962c9acc207" />


internet gateway <img width="960" height="472" alt="{677DBC5C-8C22-4C38-85A3-742F9A06EDF6}" src="https://github.com/user-attachments/assets/25ff466e-a9c7-40a3-ac61-46d9d57af0b0" />

security groups <img width="959" height="474" alt="{F6972C0C-0F4C-4EB3-A553-563965177BBC}" src="https://github.com/user-attachments/assets/ca7a5515-0ddb-4512-91a3-2daddbed75d8" />
