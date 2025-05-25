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

This threat modeling process helped me a lot to see the security side of system design. I found threats I didn’t think about before, like repudiation, which I wasn’t very familiar with before this assignment. Each threat made sense when I looked at how the system components interact, and the STRIDE model gave a clear way to categorize them. I think now the system is more secure because we added mitigation ideas for all identified threats.

Overall, this step helped improve the design and made me more aware about secure software practices.
