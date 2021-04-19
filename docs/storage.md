# Storage

## Instance stores

Servers have somewhere to store things. This is the place. When the instance gets deleted, the content here gets deleted too. Good for temp files or things that are ok to be lost.

## Elastic Block Store (EBS)

A virtual harddrive that is attached to EC2s. Allows incremental backups ('snapshots'). I guess a use for this would be application data before being saved somewhere else/to S3. Only uploads things that got changed (think online video editor). Only 1 AZ can access. Does not scale.

## S3

### Standard

Things are stored here like a file system. #Orgnisation. 5TB upload.

### IA

For stuff that isn't frequently accessed, but needs rapid access.

### One Zone-IA

Like IA, but only in 1 data centre.

### Glacier

For non-rapid access. Retrival between minutes to hours.

### Glacier deep archive

For archive with really infrequent access. Can access things within 12 hours.

## Intelligent-Tiering

Can move things in S3 between different storage tiers based on access patterns.

This is done by AWS and the user can't specify the times.

### Life-cycle policy

Like the above, but the user can define when items should be moved.

## Elastic File System (EFS)

Shared file storage. Think shared file system in work. Windows does a thing like this (shared drives?) or something like that. Region access. Scales.

