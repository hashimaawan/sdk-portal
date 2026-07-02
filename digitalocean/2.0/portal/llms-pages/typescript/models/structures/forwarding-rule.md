# Forwarding Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZvcndhcmRpbmdSdWxl

An object specifying a forwarding rule for a load balancer.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ForwardingRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificateId` | `string \| undefined` | Optional | The ID of the TLS certificate used for SSL termination if enabled. |
| `entryPort` | `number` | Required | An integer representing the port on which the load balancer instance will listen. |
| `entryProtocol` | [`EntryProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/entry-protocol.md) | Required | The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `targetPort` | `number` | Required | An integer representing the port on the backend Droplets to which the load balancer will send traffic. |
| `targetProtocol` | [`TargetProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/target-protocol.md) | Required | The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `tlsPassthrough` | `boolean \| undefined` | Optional | A boolean value indicating whether SSL encrypted traffic will be passed through to the backend Droplets. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  EntryProtocol,
  ForwardingRule,
  TargetProtocol,
} from 'digitalocean-apilib';

const forwardingRule: ForwardingRule = {
  entryPort: 443,
  entryProtocol: EntryProtocol.Https,
  targetPort: 80,
  targetProtocol: TargetProtocol.Http,
  certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
  tlsPassthrough: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



