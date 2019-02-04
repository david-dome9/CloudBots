# CloudBots

# Overview

What are D9 cloudbots?

Dome9 CloudBots are an automatic remediation solution for AWS built on top of Dome9's Continuous Compliance capabilities

Why and when would I need it?

If you have configured Dome9 Continuous Compliance policies for your cloud account, the Dome9 Compliance Engine continuously scans  your cloud account (AWS,Azure,GCP) for policy violations, and issues alerts and report for any issues that are found.

CloudBots provide automatic-remediation for compliance issues in your cloud account, in which you configure your cloud account to  take specifiic remedial actions, using cloudbots, in response to specific compliance violations. The cloudbots typically are scripts, which perform actions on your cloud account.


This approach could reduce the load on security operators and significantly reduce the time to resolve security issues.

How does it work?

Dome9 continuously  scans your cloud accounts (using compliance policies)  and sends findings for  failed rules to an AWS SNS.

To add a remediation step for a compliance rule, the rule is modified to include  a "remediation flag" in the compliance section, so that the SNS event is tagged with the remedial action. The tag indicates the bot to run if the compliance rule fails.

You configure your cloud account (or multiple accounts) with an AWS Lambda function that is invoked if a rule fails. The  Lambda function will check the rule for the remediation flag, and run the bot .

The results of bot actions are posted to the SNS.

# Onboarding

You can deploy the CloudGuard Dome9 Cloudbots in any AWS account (or accounts), whether the account is protected by CloudGuard Dome9 or not. Two procedures are included below, for both options.

You can deploy the cloudbots in any AWS region. You must deploy it separately in each region in which you want it to work.	

## Deploy in a cloud account protected by Dome9

## Deploy in a cloud account not protected by Dome9

## Use the CloudBots in accounts not protected by CloudGuard Dome9



# Prerequisites

# Use-case example
