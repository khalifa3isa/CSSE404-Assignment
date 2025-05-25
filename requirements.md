System Requirements Specification

Functional Requirements
FR1: Secure Transaction Processing
The system needs to be able to process all kinds of financial transactions like when people transfer money between accounts or pay there bills. All transactions should use strong encryption (were using AES-256) and the system has to keep logs of everything. Also it needs to detect fraud really fast - like within 100 milliseconds when someones trying to do something suspicious.

FR2: Multi-Factor Authentication (MFA)
Users should have to prove who they are with atleast two different methods especially for big transactions over $500. This could be there password plus a fingerprint scan or maybe a code sent to there phone. The whole authentication thing shouldnt take more then 30 seconds and if someone doesnt do anything for 15 minutes the system should log them out automatically for security.



Non-Functional Requirements
NFR1: Performance - Transaction Processing Speed
The system has to be really fast - like 95% of transactions need to complete in under 2 seconds. During busy times we might have 10000 people all trying to do stuff at once so the system needs to handle that. Even during the busiest hours (usually 9am to 5pm) everything should still work in less then 3 seconds.

NFR2: Security - Data Encryption Standards
All the important data needs to be encrypted when its stored (using AES-256) and when its being sent around (using TLS 1.3 or newer). We have to change the encryption keys every 90 days to keep things secure. Also were supposed to follow FIPS 140-2 Level 3 standards which is a government thing about cryptography.
