# IAM Section

## Introduction
Root account - created by default should not be used or shared (only to create other accounts)
- users: are people within organisation and can be grouped

- Groups: only contain users not other groups. 

Users can belong to 0, 1, n groups

### IAM permissions
users and groups can be assigned permissions via JSON documents called policies
    JSON documents called policies define the permissions of the users 

in AWS you apply the least privilege principle

There are already many policies definied in AWS

Tags are everywhere in AWS

Permissions are inhereted by groups.

### AWS Console simultaneous sign-in
multi sessions support; log into several accounts in a single browser session