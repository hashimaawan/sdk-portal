# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGT3ZlcnZpZXc

Placement groups are used to influence the location of interdependent virtual servers in our data centers. The distribution of the different instances within a group is based on a pattern specified in the type. By enforcing certain rules on the placement of instances within our infrastructure, availability can be influenced in a way that fits your needs best.

In `spread` placement groups, all virtual servers will run on different physical servers. This decreases the probability that some instances might fail together.


# Get Instance

The instance of the `PlacementGroupsApi` class can be accessed from the API Client.

```
placementGroupsApi := client.PlacementGroupsApi()
```



