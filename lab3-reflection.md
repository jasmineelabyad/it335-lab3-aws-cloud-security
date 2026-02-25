# Lab 3 – AWS Cloud Security Reflection

In this lab, I configured a basic AWS environment while applying foundational cloud security controls inspired by the Capital One breach case study.

For Identity and Access Management, I created an IAM user and group with restricted permissions rather than continuing to use the root account. This demonstrates least privilege because the IAM user only has access to required services instead of full administrator rights. In the Capital One breach, overly broad IAM permissions allowed the attacker to access far more data than necessary. Using limited IAM roles reduces the blast radius of compromised credentials.

For S3 storage, I created a bucket with Block Public Access enabled and verified permissions through the bucket settings. This prevents accidental exposure of sensitive data. Capital One’s breach involved improperly secured cloud resources, showing how misconfigured storage can lead to massive data leaks. Blocking public access and reviewing bucket policies are essential to protecting cloud data.

I also launched a Free Tier EC2 instance and configured its security group to allow SSH only from my specific IP address instead of open access from anywhere. This minimizes attack surface and prevents unauthorized connections. Capital One’s attacker used SSRF to access metadata services. Limiting inbound rules and being aware of IMDS settings reduces similar risks.

For monitoring and visibility, I reviewed the Billing Dashboard and CloudTrail. These services provide insight into account activity and costs. Without continuous monitoring, attackers can operate undetected for long periods, as seen in the Capital One incident. CloudTrail and billing alerts help shorten the window of opportunity by revealing suspicious activity and unusual spending.

This lab showed how easy it is to misconfigure cloud resources if proper governance is not followed. While AWS provides strong security tools, organizations must actively apply them. Organizational culture plays a major role—security controls must be enforced consistently, not treated as optional. Overall, this lab demonstrated how IAM, S3, EC2, and monitoring work together to create a secure cloud foundation and how failures in these areas contributed directly to the Capital One breach.
