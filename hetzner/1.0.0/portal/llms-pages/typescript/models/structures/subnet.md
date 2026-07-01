# Subnet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlN1Ym5ldA

*This model accepts additional fields of type unknown.*


# Interface Name

`Subnet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gateway` | `string` | Required | Gateway for Servers attached to this subnet. For subnets of type Server this is always the first IP of the network IP range. |
| `ipRange` | `string \| undefined` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `type` | [`Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Subnet, Type42 } from 'hetzner-cloud-apilib';

const subnet: Subnet = {
  gateway: '10.0.0.1',
  networkZone: 'eu-central',
  type: Type42.Server,
  ipRange: '10.0.1.0/24',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



