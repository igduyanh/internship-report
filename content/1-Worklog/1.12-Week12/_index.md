---
title: 'Week 12 Worklog'
date: 2026-07-06
weight: 12
chapter: false
pre: ' <b> 1.12. </b> '
---

### Week 12 Objectives:

- Build a centralized monitoring system for the entire architecture.
- Test and evaluate the operational capability of the Security Operations Center system.
- Finalize deployment documentation and summarize project results.

### Tasks to Complete This Week:

| Day | Task | Start Date | Completion Date | Reference |
| --- | ------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| Monday | - Build Amazon CloudWatch Dashboard for centralized monitoring.<br>- Design Dashboard to display security and system operational metrics. | 06/07/2026 | 06/07/2026 | https://docs.aws.amazon.com/cloudwatch/ |
| Tuesday | - Configure Amazon CloudWatch Alarms.<br>- Test the email alert functionality via Amazon SNS. | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/cloudwatch/ |
| Wednesday | - Research and configure CloudFront & WAF.<br>- Perform attack simulation scenarios to evaluate the system.<br>- Inspect Security Findings on Amazon GuardDuty and AWS Security Hub. | 08/07/2026 | 08/07/2026 | https://docs.aws.amazon.com/guardduty/ |
| Thursday | - Evaluate the efficiency of the Detect → Respond → Recover process.<br>- Optimize IAM Policies following the Least Privilege principle to enhance security. | 09/07/2026 | 09/07/2026 | https://docs.aws.amazon.com/iam/ |
| Friday | - Finalize deployment documentation and system user manuals.<br>- Estimate operational costs and propose future scaling options. | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/wellarchitected/ |

### Week 12 Results:

- Completed the creation of the Amazon CloudWatch Dashboard, providing a centralized monitoring interface for the entire system.
- The Dashboard displays all critical metrics, including:
  - GuardDuty Findings
  - Security Hub Findings
  - Lambda Invocations
  - Step Functions Executions
  - EC2 Health
  - WAF Blocked Requests
  - CloudFront Requests
  - ALB Request Count
- Successfully configured Amazon CloudWatch Alarms and verified stable email notification delivery via Amazon SNS.
- Conducted several attack simulation scenarios to evaluate the system's detection, response, and incident resolution capabilities.
- Confirmed that the Detect → Respond → Recover process operates exactly as designed and meets requirements.
- Optimized IAM Policies following the Least Privilege principle to restrict unnecessary access and enhance safety.
- Evaluated deployment costs and proposed extension directions such as Multi-AZ, Multi-Account, Infrastructure as Code, Amazon Macie, and Amazon Detective.
- Finalized the summary report, deployment documentation, and user guides, ensuring readiness for handover and operation.
