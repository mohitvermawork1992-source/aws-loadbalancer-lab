\# AWS Load Balancer Lab



\## Architecture

Internet → Application Load Balancer (ALB) → EC2 Instances

Also includes Network Load Balancer (NLB) for TCP traffic.



\## Steps

1\. Created 5 EC2 instances

2\. Created Application Load Balancer (public)

3\. Created Network Load Balancer (internal)

4\. Configured Security Groups:

&nbsp;  - ALB open on 80 to Internet

&nbsp;  - EC2 open on 80 only from ALB

5\. Tested:

&nbsp;  - ALB DNS works in browser

&nbsp;  - EC2 blocked from direct Internet

&nbsp;  - NLB tested using nc command



\## Test Result

✅ ALB HTTP works  

✅ Security group rules applied successfully  

✅ NLB TCP check passed



