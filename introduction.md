# Introduction

## History IT Cloud
amazon infrastructure 2002: SQS first offering
2007 launched in europe

AWS leader in gartner magic quadrant

31% of the market vs amazon 25%

use case ckoud: enterprise it, backup, big data analytics

# AWS global infra
Different infra points:
  - AWS Regions
  - AWS availability zones
  - AWS data centers
  - AWS edge locations/ points of presence

[Details|https://infrastructure.aws]

AWS regions: us-east-1; eu-west-3 
a clusters of data centers, most aws services are region-scoped

! chose a regions:
1) compliance - e.g. it has to be somehwere
2) proximity - due to latency, 
3) Availibility services within a region
4) Pricing - pricing varies per region

AWS Availability zones
Each region has many availability zones usually 3; min 3, max 6

Each availability zones is one or more discrete data centers with redundant power, networking and connectivity

So: Region Sydney: ap-southeast-2

Availability zones:
  - ap-southeast-2a (2datacenters), 
  - ap-souteast-2b (2 datacenters), 
  - ap-southeast-2c (2 datacenters)

They (AZ's) are isolated from each other so isolated from disasters (and they are connected via high speed cables)

AWS points of presence (edge locations): 400+ 

Tour of the AWS console 
global services: IAM, route53, cloudfront, WAF
region scopes: Lambda, EC2, etc

# AWS Console
selections you can make: 
regions, services, 

aws global infrastructure: aws regional services list 
    - some services are not available in each region