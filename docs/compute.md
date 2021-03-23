# EC2

The tldr is it's a virtual machine. Like getting a dedicated server but it's not. You do all the normal stuff with it such as picking an OS, doing all the config, sshing in and all of that stuff.

## Types

There are tYpEs of these, because of course there are.

### General purpose

Good for 

* Application servers
* Gaming servers
* Backend for enterprise shit.
* Small/medium databases

### Compute

When you need CPU, as if that wasn't obvious. It says you can also use these for web and gaming servers too, but iDeAl for hIgH pEfOrMaNcE (again, if it wasn't obvious) things. Tldr, if you need the cpu, use this.

### Memory optimized

Good, I guess, if you're doing something that processes large bits of data in memory. Idk, I guess a big SQL command?

The examples it gives are things like real-time processing. Maybe like ATC?

### Accelerated computing

Use accelerators (no shit) to make things more eFfIcEnT. The examples it gives are for floating-point numbers (so maths), graphics processing (idk, rendering?) and data pattern matching (idk, I guess like facial recognition?).

### Storage optimized

Good for things that are doing lots of read/write things, or large data sets. Maybe also real-time? Idk it doesn't give examples.

## Pricing

Cause, while AWS usually names things so you can tell what they are, other things not so much. You really do have to be an AWS salesman to remember all of this.

### On-demand

For short term, irregular things that can't be interupted. Run until stopped. Maybe good for developing and testing things, like a staging enviorment I guess.

### Savings plans

Reads like a NordVPN ad on YouTube. Is your usage rather consistant? Why not commit ~~murder~~ for 1 or 3 years and you can save up to 70% on your bill.

### Reserved

Also reads like a NordVPN ad? It seems like a combination of On-demand and Savings. It's a discount for On-demand use?

This one doesn't make sense. So you can get `Standard Reserved` and `Convertible Reserved` for 1 or 3 years, and `Scheduled Reserved` for 1 year?

Why? If on-demand is meant to be for short term, why commit for 1 or 3 years?

### Spot

For things with flexible start/end times that are ok with being interrupted. See this is what should be called 'on demand'.

The difference between this and on-demand is if your thing can be interupted, use spot. If not, use on-demand.

### Dedicated hosts

This is where the server is fully yours. No virtual one like normal EC2.

This fucks me up because they use `instances` to mean type of servers, but this is a price model. But **dedicated servers** are a thing themselves.

So, **this should, 100%, be a server** (fuck you 'instance') **type, not a price model term**. If you look at any other hosting company it's set this way.

## Scaling

I really don't need to explain this to myself. More demand? More servers. Less demand? Less servers?

### Auto scaling

Does this for you - wait, hold your hats - automatically. And, get this, there is

#### Dynamic

Which is, as I said, more demand, more servers. Less demand, less servers.

#### Predictive

Predicted demand. Training doesn't say if this is done by you, or AWS.

!!! important "Vertical or horizontal?"
    Vertical (or up/down) is adding more power. Horizontal is adding more of them.

# ELB

**Elastic Load Balancing**. This is the load balancer. It does the balancing on the current instances and (I think) it tells the auto scaliler to actually boot up a new instance.

# SNS

Publish/subscribe. Send messages between parts of a system. Push notifications, emails, text messages, order updates, all that kind of stuff.

# SQS

Queue system. System 1 pushes to queue, queue holds them then passes to message 2. Good if 2 gets overloaded or stops.

# Lambda

Like EC2, but you just upload the code and it runs when triggered. Meant for things under 15 minutes. You don't need to manage the underlying OS and such.

# Elastic Container Service (ECS)

Run container (think, Docker) things. It's a management tool of sorts where you push to this (or EKS) and that pushes to EC2 of Fargate.

# Elastic Kubernetes Service (EKS)

Like ECS, but for Kubernetes. It's a management tool of sorts where you push to this (or ECS) and that pushes to EC2 of Fargate.

# Fargate

Serverless ECS.