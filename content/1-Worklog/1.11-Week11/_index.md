---
title: 'Worklog Week 11'
date: 2026-06-29
weight: 11
chapter: false
pre: ' <b> 1.11. </b> '
---

### Objectives for Week 11:

- Complete the automated incident response workflow on AWS.
- Integrate serverless services into a unified and streamlined response pipeline.
- Test the incident response workflow against various types of Security Findings to evaluate its reliability.

### Tasks Planned for This Week:

| Day | Task | Start Date | Completion Date | Reference |
| --- | ------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ------------------------------------------- |
| Monday | - Finalize the AWS Step Functions workflow for incident response orchestration.<br>- Connect Amazon EventBridge with AWS Step Functions to trigger automated workflows. | 29/06/2026 | 29/06/2026 | https://docs.aws.amazon.com/step-functions/ |
| Tuesday | - Develop a Lambda function to isolate EC2 instances using an Isolation Security Group.<br>- Test the EC2 isolation workflow. | 30/06/2026 | 30/06/2026 | https://docs.aws.amazon.com/ec2/ |
| Wednesday | - Develop a Lambda function to disable compromised IAM Access Keys.<br>- Block AWS Management Console access for IAM users when credential compromise is detected. | 01/07/2026 | 01/07/2026 | https://docs.aws.amazon.com/iam/ |
| Thusday | - Store incident response history in Amazon S3.<br>- Record workflow execution logs in Amazon CloudWatch Logs. | 02/07/2026 | 02/07/2026 | https://docs.aws.amazon.com/s3/ |
| Friday | - Perform end-to-end testing of the Detect → Respond workflow using GuardDuty Sample Findings and AWS Security Hub Findings. | 03/07/2026 | 03/07/2026 | https://docs.aws.amazon.com/guardduty/ |

### Week 11 Achievements:

- Successfully completed the automated incident response workflow using AWS Step Functions.
- Configured Amazon EventBridge to automatically trigger AWS Step Functions whenever AWS Security Hub generates Security Findings.
- Developed a Lambda function that automatically isolates compromised EC2 instances by applying an Isolation Security Group.
- Implemented automated remediation to disable IAM Access Keys and block AWS Management Console access for IAM users when credential compromise is detected.
- Stored incident response records in Amazon S3 to support auditing and post-incident investigations.
- Logged all Lambda function and AWS Step Functions execution activities to Amazon CloudWatch Logs for monitoring and troubleshooting.
- Successfully validated the complete automated response pipeline: Security Hub → EventBridge → Step Functions → Lambda → SNS.
