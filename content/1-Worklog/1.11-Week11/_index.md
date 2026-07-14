---
title: 'Week 11 Worklog'
date: 2026-06-29
weight: 11
chapter: false
pre: ' <b> 1.11. </b> '
---

### Week 11 Objectives:

- Finalize the automated incident response workflow on AWS.
- Integrate serverless services into a unified and seamless workflow.
- Test the system's response capability against various types of Security Findings.

### Tasks to Complete This Week:

| Day | Task | Start Date | Completion Date | Reference |
| --- | ------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ------------------------------------------- |
| Monday | - Finalize coordination workflow using AWS Step Functions.<br>- Establish integration between Amazon EventBridge and AWS Step Functions to trigger the automated response. | 29/06/2026 | 29/06/2026 | https://docs.aws.amazon.com/step-functions/ |
| Tuesday | - Develop a Lambda Function to isolate the EC2 instance using an Isolation Security Group.<br>- Test and verify the EC2 isolation process after detecting an incident. | 30/06/2026 | 30/06/2026 | https://docs.aws.amazon.com/ec2/ |
| Wednesday | - Develop a Lambda Function to automatically disable IAM Access Keys.<br>- Block the console login access of the compromised IAM User. | 01/07/2026 | 01/07/2026 | https://docs.aws.amazon.com/iam/ |
| Thursday | - Store incident response history on Amazon S3.<br>- Record execution logs of the entire workflow on Amazon CloudWatch Logs. | 02/07/2026 | 02/07/2026 | https://docs.aws.amazon.com/s3/ |
| Friday | - Test the end-to-end Detect → Respond workflow using GuardDuty Sample Findings and Security Hub Findings to evaluate system behavior. | 03/07/2026 | 03/07/2026 | https://docs.aws.amazon.com/guardduty/ |

### Week 11 Results:

- Finalized the automated incident response workflow using AWS Step Functions, ensuring the coordination of execution steps according to design.
- Configured Amazon EventBridge to automatically trigger AWS Step Functions as soon as AWS Security Hub generates Security Findings.
- Successfully built a Lambda Function to isolate EC2 instances via an Isolation Security Group, limiting the potential spread of incidents.
- Completed the capability to automatically disable IAM Access Keys and block console login access for IAM Users showing signs of credential compromise.
- Stored all incident response history on Amazon S3, supporting audit and post-incident investigation.
- Logged the execution history of Lambda Functions and AWS Step Functions to Amazon CloudWatch Logs for monitoring.
- Successfully tested the complete automated response flow: Security Hub → EventBridge → Step Functions → Lambda → SNS, ensuring all components operate synchronously and stably.
