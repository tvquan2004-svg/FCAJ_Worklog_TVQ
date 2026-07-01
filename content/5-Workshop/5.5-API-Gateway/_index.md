---
title : "Access S3 from On-premises"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

#### Using Interface endpoint

In this section, you will create **an Interface endpoint** to access **Amazon S3** from **an on-premises environment**. Unlike the Gateway endpoint, Interface endpoints use PrivateLink and are accessible from on-premises via VPN or Direct Connect.

To set up the Interface endpoint, you will configure the necessary security groups, create the endpoint, and test connectivity from the simulated on-premises environment.

#### Content

- [Prepare environment](5.4.1-prepare/)
- [Create Interface endpoint](5.4.2-create-interface-endpoint/)
- [Test endpoint](5.4.3-test-endpoint/)
- [DNS simulation](5.4.4-dns-simulation/)
