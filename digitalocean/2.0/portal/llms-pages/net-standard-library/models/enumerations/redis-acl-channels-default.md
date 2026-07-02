# Redis Acl Channels Default

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlZGlzQWNsQ2hhbm5lbHNEZWZhdWx0

Determines default pub/sub channels' ACL for new users if ACL is not supplied. When this option is not defined, all_channels is assumed to keep backward compatibility. This option doesn't affect Redis configuration acl-pubsub-default.


# Enum Type Name

`RedisAclChannelsDefault`


# Fields

| Name |
|  --- |
| `Allchannels` |
| `Resetchannels` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

RedisAclChannelsDefault redisAclChannelsDefault = RedisAclChannelsDefault.Allchannels;
```



