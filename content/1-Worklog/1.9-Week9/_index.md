---
title: 'Week 9 Worklog'
date: 2026-06-15
weight: 9
chapter: false
pre: ' <b> 1.9. </b> '
---

### Week 9 Objectives:

- Build a basic security monitoring environment on AWS.
- Configure logging, monitoring, and threat detection services to track system activities.

### Tasks Completed During the Week:

| Day | Task Description | Start Date | End Date | Reference |
|-----|------------------|------------|----------|-----------|
| Monday | - Create an AWS account and enable Multi-Factor Authentication (MFA) for the Root User.<br>- Create an IAM User with the `AdministratorAccess` policy for day-to-day administrative tasks. | 15/06/2026 | 15/06/2026 | https://docs.aws.amazon.com/iam/ |
| Tuesday | - Enable AWS CloudTrail to record all API calls within the AWS account.<br>- Configure VPC Flow Logs and deliver log data to Amazon CloudWatch Logs. | 16/06/2026 | 16/06/2026 | https://docs.aws.amazon.com/cloudtrail/ |
| Wednesday | - Enable AWS Config to monitor configuration changes to AWS resources.<br>- Configure AWS Budgets and create monthly cost alerts. | 17/06/2026 | 17/06/2026 | https://docs.aws.amazon.com/config/ |
| Thursday | - Enable Amazon GuardDuty in the `ap-southeast-1` Region.<br>- Enable AWS Security Hub with the NIST 800-53 security standard.<br>- Integrate GuardDuty findings into AWS Security Hub. | 18/06/2026 | 18/06/2026 | https://docs.aws.amazon.com/securityhub/ |
| Friday | - Enable IAM Access Analyzer.<br>- Create CloudWatch Alarms to monitor failed sign-in attempts and Root User activity.<br>- Generate GuardDuty sample findings and verify that the alerts appear correctly in AWS Security Hub. | 19/06/2026 | 19/06/2026 | https://docs.aws.amazon.com/guardduty/ |

### Achievements:

- Implemented fundamental IAM security best practices by enabling MFA for the Root User and using an IAM User with administrative privileges for daily operations.
- Enabled AWS CloudTrail to record all API calls made within the AWS account.
- Configured VPC Flow Logs to collect network traffic logs and deliver them to Amazon CloudWatch Logs.
- Enabled AWS Config to monitor and record configuration changes to AWS resources.
- Configured AWS Budgets with monthly cost alerts to help monitor and control AWS spending.
- Enabled Amazon GuardDuty to detect suspicious activities and potential security threats.
- Configured AWS Security Hub and integrated GuardDuty findings into a centralized security management dashboard.
- Enabled IAM Access Analyzer to identify AWS resources that are shared externally.
- Created CloudWatch Alarms to monitor critical events, including failed sign-in attempts and Root User activity.
- Generated GuardDuty sample findings and verified that the alerts were successfully displayed in AWS Security Hub.
