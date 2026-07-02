# Entry Protocol

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkVudHJ5UHJvdG9jb2w

The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly.


# Enum Type Name

`EntryProtocol`


# Fields

| Name |
|  --- |
| `HTTP` |
| `HTTPS` |
| `HTTP2` |
| `HTTP3` |
| `TCP` |
| `UDP` |


# Example

```php
use DigitalOceanApiLib\Models\EntryProtocol;

$entryProtocol = EntryProtocol::TCP;
```



