# Redis Acl Channels Default

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlZGlzQWNsQ2hhbm5lbHNEZWZhdWx0

Determines default pub/sub channels' ACL for new users if ACL is not supplied. When this option is not defined, all_channels is assumed to keep backward compatibility. This option doesn't affect Redis configuration acl-pubsub-default.


# Class Name

`RedisAclChannelsDefault`


# Fields

| Name |
|  --- |
| `Allchannels` |
| `Resetchannels` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    redisAclChannelsDefault := models.RedisAclChannelsDefault_Allchannels

}
```



