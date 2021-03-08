# Shared responsibility model

Amazon looks after the underlying infrastructure. Customer looks after what they put into it.

## Customer

* Platform, applications, user access (IAM).
* OS, networking, firewall.
* Client/server side encryption, network protection.

You're responsible for the OS up.

## AWS

* Compute, storage, DBs, networking
* AWS infrastructure.

# IAM

## Root user

Master user. Ya know, like root on Linux and such.

## IAM user

A user

## IAM policy

Group of permissions in json of what a user can or can't do.

## IAM Groups

Groups of users. Policies can be applied to groups which effects all users of said group.

## IAM Role

Think, Groups but tempoary.

No username/password, but tempoary access to permissions. Can be used for

* Users
* External identities
* Applications
* Other AWS services.

When an IAM user gets a role, it loses it's previous permissions and only has the ones of the role.

!!! danger "Review this"
    The training says "when an identity assumes a role..." but it doesn't actually say what an identity is. I'm assuming an IAM user.

# Organizations

Manage all of the above but over several AWS accounts, billing, etc.

## Service control policies (SCPs).

Think, IAM policies above. Can be attached to OUs or an individual member account.

!!! danger "Review this"
    What is an "individual member account"? I would assume this to be an IAM user but training says it's not. So..what is it exactly?

## Organizational units (OU)

Think, IAM groups above.

!!! danger "Review this"
    Please confirm that my understanding of OUs and SCPs are correct.

# DDOS

## Shield (with WAF)

Machine learning, proactive defence.

### Standard

Provided to all customers at no cost.

### Advanced 

Paid, provides detailed information on attacks. Intergrates with CloudFront, Route 53 and ELB. 

# KMS

Key management, like SSL certs.

# WAF

Web application firewall.

# Inspector

Checks your application for deviations in security best practices.

# GuardDuty 

Threat detection for AWS resources and infrastructure. Watches network and account activity.