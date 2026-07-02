# Target Protocol

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlRhcmdldFByb3RvY29s

The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly.


# Enum Type Name

`TargetProtocol`


# Fields

| Name |
|  --- |
| `Http` |
| `Https` |
| `Http2` |
| `Tcp` |
| `Udp` |


# Example

```ts
import { TargetProtocol } from 'digitalocean-apilib';

const targetProtocol = TargetProtocol.Tcp;
```



