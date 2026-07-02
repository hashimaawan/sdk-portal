# Size 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNpemUy

This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.

* `lb-small` = 1 node
* `lb-medium` = 3 nodes
* `lb-large` = 6 nodes

You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.


# Enum Type Name

`Size2`


# Fields

| Name |
|  --- |
| `LBSMALL` |
| `LBMEDIUM` |
| `LBLARGE` |


# Example

```python
from digitaloceanapi.models.size_2 import Size2

size_2 = Size2.LBSMALL
```



