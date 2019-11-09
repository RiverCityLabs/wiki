---
description: >-
  a description of the proposed automations at the space to reduce the effort
  involved in running it
---

# RCL Automation

## New member invitations to slack.

1. Current State: 
   1. when a new member registers and pays for a membership, the officers look for the payment received email, then send the slack invite \(maybe type a nice welcome message\), set a reminder for 30 days to add them to the door access channel \(1 month probation\), then follow up a month later to add them to the door access channel.
2. Proposed State: 
   1. a daily script is ran that pulls the latest membership data from our membership management site, determines if anyone become members the previous day, determines if anyone needs to be added to the door access channel, and sends out slack invites as necessary.

## Self Service Portal

1. Current State
   1. creating a new gsuite user is manual
2. Proposed State
   1. Some kind of self service google form that allows RCL members to request a Gsuite account, or any other account or service so an officer doesn't need to.

## Validating payments and memberships

1. Current State:
   1. I have a number of different membership status items for each member in civicrm: current, grace\(overdue but less than a month\), expired \( overdue more than a month\) and canceled.
   2. I have civicrm give me a report on member status and then go on to PayPal, stripe and Braintree to see if the payments were made and record the payment date.
   3. Actually all I have to due is tell civicrm to renew the membership if the payment has been made
   4. There is a way to get civicrm to to all that automatically but I would have to integrate our payment processing system into civicrm.
2. Proposed State: TBD

## Waivers

1. Current State:
   1. We need to update liability waivers every year for every member for insurance reasons. This is a huge hassle to get everyone into the space to sign off on it. 
2. Proposed State:
   1. We should look into web based waiver solutions that can be sent automatically when they expire, eliminating any manual tasks

## Automated Maintenance Reminders

1. slash command to set up new tasks with time intervals, then post to slack when due, and daily reminders when not completed. Completed tasks no longer notified daily and are set for the next time interval

