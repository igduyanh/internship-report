---
title: 'Week 10 Worklog'
date: 2026-06-22
weight: 10
chapter: false
pre: ' <b> 1.10. </b> '
---

### Week 10 Objectives:

- Build an automated incident response system using AWS serverless services.
- Develop AWS Lambda functions to process security alerts and perform automated remediation actions.
- Integrate Amazon EventBridge to automatically trigger the incident response workflow.

### Tasks Completed During the Week:

| Day | Task Description | Start Date | End Date | Reference |
|-----|------------------|------------|----------|-----------|
| Monday | - Create an Amazon SNS topic for sending security notifications.<br>- Subscribe an email address to receive alert notifications. | 22/06/2026 | 22/06/2026 | https://docs.aws.amazon.com/sns/ |
| Tuesday | - Develop the first AWS Lambda function to process Amazon GuardDuty findings.<br>- Analyze the severity of security events and send notifications through Amazon SNS. | 23/06/2026 | 23/06/2026 | https://docs.aws.amazon.com/lambda/ |
| Wednesday | - Develop the second AWS Lambda function to automatically block suspicious IP addresses by updating Amazon EC2 security groups. | 24/06/2026 | 24/06/2026 | https://docs.aws.amazon.com/ec2/ |
| Thursday | - Create an Amazon EventBridge rule to invoke the Lambda function when Amazon GuardDuty detects **High** severity findings.<br>- Test the complete workflow from GuardDuty detection to email notification. | 25/06/2026 | 25/06/2026 | https://docs.aws.amazon.com/eventbridge/ |
| Friday | - Develop the third AWS Lambda function to automatically revoke exposed IAM access keys.<br>- Design a multi-step incident response workflow using AWS Step Functions. | 26/06/2026 | 26/06/2026 | https://docs.aws.amazon.com/step-functions/ |

### Achievements:

- Successfully configured Amazon SNS to send security alert notifications via email.
- Developed AWS Lambda functions using Python 3.12 to automatically process Amazon GuardDuty findings.
- Implemented automated email notifications based on the severity level of security events.
- Completed an automated remediation function that updates Amazon EC2 security groups to block suspicious IP addresses.
- Configured Amazon EventBridge to automatically trigger AWS Lambda functions when Amazon GuardDuty detects **High** severity threats.
- Successfully validated the end-to-end incident response workflow, including:
  - Amazon GuardDuty sample findings
  - Amazon EventBridge rules
  - AWS Lambda functions
  - Amazon SNS email notifications
- Implemented automatic revocation of exposed IAM access keys when compromised credentials are detected by Amazon GuardDuty.
- Designed a multi-step incident response workflow using AWS Step Functions.
- Applied AWS security best practices, including:
  - Using IAM roles instead of embedding access keys in source code.
  - Logging execution details to Amazon CloudWatch Logs.
