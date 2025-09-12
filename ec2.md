# EC2 fundamentals

## Budget setup
Alarm and budget setup to not overspent
admin access no default budget access --> Can access billing info on checkmark

budget can be used to sent alert when overspent

## EC2 basics
EC2 popular offering: Elastic compute cloud - infra as a service
- VM's
- Store data - EBS
- load control - ELB
- scaling the services using auto-scaling group (ASG)

OS options: Linux, MacOS, windows

CPU, RAM, storage, network, security grouo, EC2 user data

### EC2 user data
it's possible to bootscrap instances using EC2 user data script 
bootstrapping means launching commands when a machine starts 
automate boot tasks (install updates, software, downloading files)

bootstrap runs on root user
Amazon Linux as OS 
security group - allows control to and from instances (basically the firewall)
volumes can be deleted on deletion of the EC2 instances

Userdata is on the instances options 
private ip-adress of the machine is on the AWS cloud, public on the internet

stop and start instance: will change the public ip-address (so its not allocated)

### EC2 instacne types basics
Different instance types have different use cases:
general, compute optimizes, memory optimized, accelerated optimized

m5.2xlarge

m: instance class memory 
5: generation (AWS imrpoves over time)
2xlarge: size within instance class

general: web servers, code repo's. They are balanced
    e.g. T4g, T2
compute: high processr: batch processing workloads, media transcoding, high performance webservice, high performance computing, machine learning 
    e.g. C6g, C5a, C4
memory: fast : high performance in memeory db's, web scale cache store, BI, apps for real-time of big unste
    e.g. R6g, R5b, R5n   R=RAM
storage optimed: databases on disk, high frequency online transaction processing systems, Redis
    e.g. i

comoaring instances: Ec2 instances.info 

### Security groups
SG's are fundamental of network security 
They control how traffic is allowed into or out of EC2 

- Security groups only contain allow rules
- Security group rules can be referenced by IP or by security group

they regulate:
- access to ports
- authorized ip ranges
- contron inbound traffic
- control outbound traffic 

good to know:
- can be attached to multiple instances
- locked down to a regio/ VPC combination
- lives outsice the EC2
- it;s good to maintant one seperate SG for SSH
- it app it not accessible (timeout) then its a security group issue
- conenction refused is NOT a security group issue
- default all inbound blocked
- default all outbound allowed


You can reference secuirty groups from other security groups:
    if EC2 A has SG1 attached you can say in SG2 attached to EC2 B that SG1 is allowed to access EC2 B. 
    so you dont have to think about IP addresses

Classic ports good to know:
22 SSH
21 FTP
22 sFTP
80 HTTP
443 HTTPS
3389 RDP remote desktop protocol

### SG handson

timeout is most likely sg

### SSH summary table

ssh cannot be 
EC2 instances connect: works for all machines

EC2 instances connect : connect via browser 

### IAM roles demo
instance user connect: ec2-user 

EC2 AWS linux had AWS CLI preinstalled

couple the IAM role to our EC2 instance ()

### Ec2 instances purchase options
- short workloads on-demand predictable, pay per second
- reserved instances : 1 or 3 years 
    reserved instances - long workloads
    convertable reserved instances - long workloadfs with flexible instances 
- saving plan: 1 or 3 yeards: commitment to an amount of usage long workload (to dollar ammount)
- spot instances - short workload cheap and can be lost
- dedicated hiosts - entire physical server, control instance placement
- dedicated instancesno other customer will share your hardware
- capacity reservation: in a specific AZ  for any duration

#### On demand
 - pay for what you you (highest cost) no upfrront reservation
 - highest cost, no long term commitment 


#### reserved instance 
- 72% discount
- you reserve a specifif instance attributes
- 1 or 3 years
- upfront, partially upfront, not upfrant
- reserved instances scope - regional or zonal
- recommended for steady state usage
- buy or sell in marketplace
- convertible little less discount

#### EC savings plan
- discount on long term
- commitment to a certain type of usage ($10 oer hour)
- beyond savings plan : on demand pricing

#### spot instances
- can be lost
- most cost efficient
- distributed workload
- not for critical jobs/ databases

