---
title: 'Week 10 Worklog'
date: 2026-06-22
weight: 10
chapter: false
pre: ' <b> 1.10. </b> '
---

### Week 10 Objectives:

- Build an automated incident response system based on serverless AWS services.
- Develop AWS Lambda Functions to process security alerts and automatically implement remediation tasks.
- Integrate Amazon EventBridge to trigger the automated incident response workflow.

### Tasks to Complete This Week:

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | ------------ | --------------- | --------------- |
| Monday | - Create an Amazon SNS Topic for sending security alerts.<br>- Subscribe an email address to receive notifications. | 22/06/2026 | 22/06/2026 | https://docs.aws.amazon.com/sns/ |
| Tuesday | - Develop the first AWS Lambda Function to process GuardDuty Findings.<br>- Analyze event severity and send alerts via Amazon SNS. | 23/06/2026 | 23/06/2026 | https://docs.aws.amazon.com/lambda/ |
| Wednesday | - Develop the second AWS Lambda Function to automatically block suspicious IP addresses by updating the Security Group of Amazon EC2. | 24/06/2026 | 24/06/2026 | https://docs.aws.amazon.com/ec2/ |
| Thursday | - Create an Amazon EventBridge Rule to trigger Lambda when GuardDuty detects a High severity alert.<br>- Test the entire workflow from GuardDuty to the email alert. | 25/06/2026 | 25/06/2026 | https://docs.aws.amazon.com/eventbridge/ |
| Friday | - Develop the third AWS Lambda Function to automatically revoke compromised IAM Access Keys.<br>- Design a multi-step incident response process using AWS Step Functions. | 26/06/2026 | 26/06/2026 | https://docs.aws.amazon.com/step-functions/ |

### Week 10 Results:

- Completed Amazon SNS configuration to send security alerts via email.
- Developed AWS Lambda Functions using Python 3.12 to automatically process GuardDuty Findings.
- Built a feature to automatically send alert emails based on the severity of security events.
- Completed the feature to automatically update the Security Group of Amazon EC2 to block suspicious IP addresses.
- Configured Amazon EventBridge to automatically trigger AWS Lambda when GuardDuty detects High severity threats.
- Successfully tested the complete incident response workflow, including:
  - GuardDuty Sample Finding
  - Amazon EventBridge Rule
  - AWS Lambda
  - Amazon SNS Email Notification
- Implemented the capability to automatically revoke an IAM Access Key when GuardDuty detects compromised credentials.
- Designed a workflow using AWS Step Functions to coordinate multi-step incident response processes.
- Applied AWS-recommended security practices, including:
  - Using IAM Roles instead of storing Access Keys in source code.
  - Logging execution history to Amazon CloudWatch Logs.
