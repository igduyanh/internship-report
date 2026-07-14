---
title: 'Week 9 Worklog'
date: 2026-06-15
weight: 9
chapter: false
pre: ' <b> 1.9. </b> '
---

### Week 9 Objectives:

- Build a basic security monitoring environment on AWS.
- Configure logging, monitoring, and threat detection services to monitor system activities.

### Tasks to Complete This Week:

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | ------------ | --------------- | --------------- |
| Monday | - Enable Multi-Factor Authentication (MFA) for the Root User.<br>- Create an IAM User with `AdministratorAccess` permissions for daily administrative tasks. | 15/06/2026 | 15/06/2026 | https://docs.aws.amazon.com/iam/ |
| Tuesday | - Enable AWS CloudTrail to record all API Calls in the account.<br>- Configure VPC Flow Logs and forward logs to Amazon CloudWatch Logs. | 16/06/2026 | 16/06/2026 | https://docs.aws.amazon.com/cloudtrail/ |
| Wednesday | - Enable AWS Config to track resource configuration changes.<br>- Set up AWS Budgets and create monthly cost alerts. | 17/06/2026 | 17/06/2026 | https://docs.aws.amazon.com/config/ |
| Thursday | - Enable Amazon GuardDuty in region `ap-southeast-1`.<br>- Enable AWS Security Hub with the NIST 800-53 security standard.<br>- Integrate GuardDuty findings into AWS Security Hub. | 18/06/2026 | 18/06/2026 | https://docs.aws.amazon.com/securityhub/ |
| Friday | - Enable IAM Access Analyzer.<br>- Create CloudWatch Alarms to monitor failed login attempts and Root User usage.<br>- Generate GuardDuty sample findings and verify alerts in AWS Security Hub. | 19/06/2026 | 19/06/2026 | https://docs.aws.amazon.com/guardduty/ |

### Week 9 Results:

- Completed the configuration of basic IAM security measures by enabling MFA for the Root User and using an IAM User with administrative privileges for daily tasks.
- Enabled AWS CloudTrail to record all API Calls generated within the AWS account.
- Configured VPC Flow Logs to collect network traffic logs and forward the data to Amazon CloudWatch Logs.
- Enabled AWS Config to track and log configuration changes for AWS resources.
- Set up AWS Budgets along with monthly cost alerts to support budget control.
- Enabled Amazon GuardDuty to detect anomalous activities and potential security threats.
- Configured AWS Security Hub and integrated GuardDuty findings into the centralized security management system.
- Established IAM Access Analyzer to detect resources shared outside the AWS account.
- Created CloudWatch Alarms to monitor critical events such as failed login attempts and Root User usage.
- Generated GuardDuty sample findings and confirmed that alerts are displayed correctly in AWS Security Hub.
