Reliability Metrics Specification

Metric 1: 
System Availability Rate

Definition: 
This is basically how much time the system is actually working vs being down. You calculate it by taking the total time minus any downtime then divide by total time and multiply by 100 to get a percentage.
Target: Were aiming for 99.99% uptime which means the system can only be down for about 52 minutes per year which is not thats much.


Measurement Method:
The system checks if everythings working every 30 seconds
If something breaks we get alerts right away
Every month we make reports about any downtime and figure out what went wrong

Justification: 
People need to access there money whenever they want for example imagine if you needed to pay for something urgent and the banking system was down. That would be terrible! Also the government and regulators expect banks to have really high availability. The 99.99% target is pretty standard for important financial systems.

Metric 2: 
Mean Time Between Failures (MTBF)
Definition: 
This tells us how long the system usually runs before something breaks. You get this number by dividing how many hours the system has been running by how many times its failed.

Target: 
We want the MTBF to be atleast 2000 hours (thats about 83 days between failures)


Measurement Method:
The system automatically detects and logs when things fail
We categorize failures as critical major or minor
Every 3 months we analyze the MTBF and see if its getting better or worse

Justification: 
A high MTBF means the system is stable and doesnt break often which saves money on fixing things. For a banking system thats running 24/7 and handling peoples money all the time we really need long periods without any failures. This helps keep customers happy and meets what the regulators expect from us.
