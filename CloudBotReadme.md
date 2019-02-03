# CloudBots

# Overview

What are D9 cloudbots?

Cloud-Bots is an automatic remediation solution for AWS built on top of Dome9's Continuous Compliance capabilities

Why and when would I need it?
What does it do?

If you have configured Dome9 Continuous Compliance policies for your cloud account, the Dome9 Compliance Engine continuously scans  your cloud account (AWS,Azure,GCP) for policy violations, and issues alerts and report for any issues that are found.

CloudBots provide automatic-remediation for issues, in which you configure your cloud account to  take specifiic remedial actions, using cloudbots, in response to specific compliance violations. The actions use Dome9 cloudbots, which typically are scripts, which perform actions on your cloud account.


This approach could reduce the load from the security operators and drastically reduce the time to resolve security issues.

How does it work?

Dome9 will scan the accounts on an ongoing basis and send failing rules to SNS
In the rules, if we want to add remediation, we can add in a "remediation flag" into the compliance section so that the SNS event is tagged with what we want to do.
Each remediation bot that is tagged correlates to a file in the bots folder of the remediation function.
Lambda reads the message tags and looks for a tag that matches AUTO:
If any of those AUTO tags match a remediation that we have built out, it'll call that bot.
All of the methods are sending their events to an array called text_output. Once the function is finished working, this array is turned into a string and posted to SNS

# Onboard


# Prerequisites

# Use-case example
