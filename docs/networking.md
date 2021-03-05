# Virtual Private Cloud (VPC)

Think, your own network inside AWS.

# Internet gateway

The thing that lets internet traffic into your network.

# Virtual private gateway

Like internet gateway, but only from specific networks. Think work VPN or work intranet.

# Direct connect

Direct connection between 1 network to AWS. This seems more like a data center to AWS connection rather than the private gateway. This seems really $$$.

# Subnets

Different areas inside the VPC, public or private areas. Public has access to the internet gateway.

# Network access control list (NACL)

Every packet is checked, both in **and** out of a *subnet*. Is stateless (doesn't remembers).

# Security group

Think NACL, but for *instances*. Only checks entry, not exit (by default). Is stateful (remembers).

# Route 53

AWS's own DNS system and domain registrar.

# CloudFront

AWS CDN.