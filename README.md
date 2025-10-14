# Dynamic Website Deployment on AWS


![Alt text](Host_a_Dynamic_Web_App_on_AWS.png)

---

## Project Overview
This project demonstrates the deployment of a dynamic website on AWS using various AWS services to ensure scalability, security, and high availability. The infrastructure is designed with a Virtual Private Cloud (VPC) spanning multiple Availability Zones, leveraging an Auto Scaling Group, Load Balancer, and other AWS services.

---
## AWS Resources Utilized
### **Networking and Security**
1. **Virtual Private Cloud (VPC):** Configured with both public and private subnets across two Availability Zones.
![Screenshot 2025-02-11 054311](https://github.com/user-attachments/assets/69b4081c-67c0-45a6-a31a-67a0a01665ed)
---
2. **Internet Gateway:** Enables communication between VPC instances and the internet.
![Screenshot 2025-02-11 054414](https://github.com/user-attachments/assets/1b3a0e8d-1088-40f7-b66d-116b15d7e13c)
---
3. **Security Groups:** Serve as a network firewall mechanism to regulate inbound and outbound traffic.
![Screenshot 2025-02-11 054502](https://github.com/user-attachments/assets/7b2a5762-8665-4dc8-84c6-c90ff68e07b6)
---
4. **Availability Zones:** Two Availability Zones were used to ensure fault tolerance and reliability.
![Screenshot 2025-02-11 053757](https://github.com/user-attachments/assets/e8ed099d-376f-4dd5-9913-54daf024b0fa)
---
5. **Public Subnets:** Used for the Application Load Balancer (ALB) and NAT Gateway.
![Screenshot 2025-02-11 054325](https://github.com/user-attachments/assets/8d1cae04-23b2-4e4e-b98a-56395f3f0853)
---
6. **EC2 Instance Connect Endpoint:** Enables secure connections to assets within both public and private subnets.
![Screenshot 2025-02-11 054519](https://github.com/user-attachments/assets/cd28ef41-0eb1-48e2-9411-702608a7d325)
---
7. **Private Subnets:** Web servers (EC2 instances) are placed in private subnets for enhanced security.
![Screenshot 2025-02-11 054325](https://github.com/user-attachments/assets/bcf0f47a-4747-44e0-80ac-1078051f3e9d)
![Screenshot 2025-02-11 054340](https://github.com/user-attachments/assets/98f6b89b-37f9-4f69-97e1-a21e24ae8d68)
---
8. **NAT Gateway:** Allows instances in private subnets to access the internet while remaining secure.
![Screenshot 2025-02-11 054431](https://github.com/user-attachments/assets/cb7238b9-45ac-400a-ba98-87834fed09b9)
---
### **Compute and Scalability**
9. **EC2 Instances:** Hosted the dynamic website.
![Screenshot 2025-02-11 053757](https://github.com/user-attachments/assets/10b0be18-5ef7-46da-a801-4c4251a0cb78)
---
10. **Application Load Balancer (ALB):** Distributes incoming traffic across an Auto Scaling Group of EC2 instances.
![Screenshot 2025-02-11 050359](https://github.com/user-attachments/assets/6c305047-447f-40b3-b7ae-432f8441e2d7)
![Screenshot 2025-02-11 053821](https://github.com/user-attachments/assets/6ec9c01b-e2b0-40c3-bb16-6d4fa956d0dc)
---
11. **Auto Scaling Group:** Automatically manages EC2 instances to ensure availability, scalability, fault tolerance, and elasticity.
![Screenshot 2025-02-11 052232](https://github.com/user-attachments/assets/7f9667f8-e987-4c65-8cb9-0c591edfa044)
![Screenshot 2025-02-11 052256](https://github.com/user-attachments/assets/8a7037c8-21bc-4404-aeb8-c24996863140)
![Screenshot 2025-02-11 052756](https://github.com/user-attachments/assets/11425b09-810e-401f-8dc4-4d231385905c)
![Screenshot 2025-02-11 053500](https://github.com/user-attachments/assets/f47d08db-6666-4f5d-857a-7023b506afb7)
![Screenshot 2025-02-11 053757](https://github.com/user-attachments/assets/16790c8c-7bf0-4807-882a-429a469a8c7d)
---
### **Security and Monitoring**
12. **AWS Certificate Manager (ACM):** Secures application communications with SSL/TLS certificates.
![Screenshot 2025-02-10 063603](https://github.com/user-attachments/assets/3a01436c-15ce-42da-9568-55ead445211b)
![Screenshot 2025-02-11 051434](https://github.com/user-attachments/assets/0036260e-99c7-4b33-b9c3-0407b1abd5f6)
![Screenshot 2025-02-11 051300](https://github.com/user-attachments/assets/94ec37e4-c1a6-47a9-8b35-6d54b892e68b)
---
13. **Simple Notification Service (SNS):** Configured to send notifications regarding Auto Scaling activities.
![Screenshot 2025-02-11 054112](https://github.com/user-attachments/assets/52933a9e-83b6-474f-8aad-7ded2086459f)
---
### **Domain and Storage**
14. **Amazon RDS:** Highly scalable database for managing user data and transactions.
![Screenshot 2025-02-11 054553](https://github.com/user-attachments/assets/4c681448-6d7f-4631-9295-4cbe510939a7)
![Screenshot 2025-02-11 054622](https://github.com/user-attachments/assets/11f56bcb-97a9-4670-bb0f-aedab4f6075d)
![Screenshot 2025-02-11 050750](https://github.com/user-attachments/assets/7665c831-3dca-4fa6-8acc-04306976ee9a)
---
15. **Route 53:** Domain name registration and DNS configuration for routing web traffic.
![Screenshot 2025-02-11 054826](https://github.com/user-attachments/assets/7687fb2b-b934-4685-a3be-9c57da6ebf06)
![Screenshot 2025-02-11 054856](https://github.com/user-attachments/assets/d95cf559-39a0-4563-b14e-1b1d1e0a51f8)
---
16. **Amazon S3:** Used to store application code.
![Screenshot 2025-02-11 054236](https://github.com/user-attachments/assets/e5f5390a-ff89-4ac6-82dd-31658cd779e1)
![Screenshot 2025-02-11 054719](https://github.com/user-attachments/assets/db41abc3-7b6a-43ce-80ef-176300a2b9f2)
![Screenshot 2025-02-10 063023](https://github.com/user-attachments/assets/1426eb7b-7544-4569-9a3e-e7b85d15c516)
![Screenshot 2025-02-10 063040](https://github.com/user-attachments/assets/3cd71a2c-6ff9-4d4c-8318-767ad9d42d18)
---


## Monitoring and Alerts
- The Auto Scaling Group is configured with SNS to send notifications on instance scaling events.
- AWS CloudWatch can be used for monitoring instance performance and logging application errors.

## Conclusion
This project demonstrates a highly available, scalable, and secure architecture for hosting a dynamic website on AWS using best DevOps practices. By leveraging AWS services, I ensure seamless scalability, security, and efficient resource management.

---



