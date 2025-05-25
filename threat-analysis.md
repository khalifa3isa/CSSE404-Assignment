# Threat Analysis

## Overview

This threat analysis was done for an online banking system, where the system includes users, bank admins, web application, authentication services, transaction processor, and two data stores: a customer database and a transaction ledger. The goal of the model was to identify any possible security threats in the early design phase using Microsoft Threat Modeling Tool 2016. The STRIDE model helped us understand what kind of issues we might face like spoofing or information disclosure and more.

We created a full diagram with components and the correct data flows, mostly HTTPS and Generic Data Flow. After that, we used the auto-generate threat option and analyzed the results one by one to understand the impact of each threat and how we can reduce or fix it.

## Components Included
- User
- Bank Admin
- Web App
- Authentication Services
- Transaction Processor
- Customer Database
- Transaction Ledger

## Data Flows Used
- HTTPS for connections between users/admins and web services
- Generic Data Flow for backend communication (e.g. processor to database)

## Key Threats Identified and Mitigation Suggestions

| STRIDE Category         | Example Threat                                 | Mitigation Strategy                                |
|-------------------------|------------------------------------------------|----------------------------------------------------|
| Spoofing                | Someone pretending to be a real user           | Use MFA (like OTP), secure login methods           |
| Tampering               | Transactions could be changed mid-way          | Use secure protocols, hashing, and input checks    |
| Repudiation             | A user might deny doing a transaction          | Logging actions, timestamps, and record tracking   |
| Information Disclosure  | Sensitive data could leak                      | TLS, encrypted database, limit access rights       |
| Denial of Service       | System may crash from too many requests        | Add rate limiting, WAF, and load balancing         |
| Elevation of Privilege  | Gaining higher access than allowed             | Strong access control and permissions management   |

## Summary

This threat modeling stuff really helped me understand the security side of designing systems better. I found a bunch of threats I didnt even think about before - like repudiation which I honestly had no idea what that was until this assignment. Once I started looking at how all the different parts of the system talk to each other the threats started making more sense. The STRIDE model was actually pretty useful for organizing everything instead of just randomly thinking about what could go wrong.

I think the system is way more secure now that we added all those mitigations for the threats we found. Its kind of crazy how many ways hackers could attack a banking system if you dont plan for it. This assignment definitely made me realize how important it is to think about security from the beginning not just add it at the end.
