# RCA 1: HTTP Port 80 Blocked in Security Group

- *Environment:* AWS ap-southeast-2, lab-vpc, lab-web-server (i-05d7ca899cf28e77d), public IP 13.239.236.105
- *What Happened:* Removing inbound HTTP (port 80) access caused requests to http://13.239.236.105 to fail/time out.
- *Root Cause:* Security group inbound rules blocked external HTTP traffic on port 80 before it could reach Nginx.
- *Resolution:* Restored inbound HTTP (port 80) on the security group and refreshed http://13.239.236.105 to confirm *Cloud Lab Web Server Live* returned.
- *Takeaway:* Always check security group rules first when a running instance stops responding to HTTP traffic.
