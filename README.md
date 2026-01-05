

#AWS IAM Foundations: Managing Users, Groups, and Permissions

📌 Project Overview

This project demonstrates the implementation of AWS Identity and Access Management (IAM) to secure an AWS environment. By moving away from using the Root user for daily tasks, this lab focuses on creating a secure, scalable hierarchy of users and groups with granular permissions.

🎯 Lab Objectives

By completing this project, I successfully achieved the following:

IAM Infrastructure: Explored and managed IAM Users and Groups.
Security Policies: Inspected and applied IAM policies to groups to enforce permissions.
Real-World Scenario: Followed a hands-on scenario to add users to specific groups and validated their access levels.
Access Management: Located and utilized the unique IAM sign-in URL for delegated access.
Service Validation:Experimented with various policies to confirm service-level access (e.g., S3, EC2).

 🛠 Solution & Approach

To fulfill the project requirements, I followed a structured administrative workflow:

1. Group Creation: Created functional groups (e.g., `S3-Admins`, `Read-Only-Users`) to manage permissions at scale rather than individually.
2. Policy Attachment: Attached AWS Managed Policies to these groups to define what actions members can perform.
3. User Provisioning: Created IAM users and assigned them to their respective groups, ensuring they inherited the correct permissions.
4. Testing & Verification:Logged in via the IAM-specific Sign-in URL to verify that users could only access the services permitted by their group policy.

⚙️ Key Configurations

IAM Policy Example (Least Privilege)

Below is an example of a JSON policy used during the lab to grant read-only access to S3 buckets:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:Get*",
                "s3:List*"
            ],
            "Resource": "*"
        }
    ]
}

```

 📸 Project Documentation (Screenshots)





🔗 Relevant AWS Documentation

[IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
[AWS IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
[IAM Policy Reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies.html)


