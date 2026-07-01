# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q


# Interface Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipRange` | `string \| undefined` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `type` | [`Type42Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `vswitchId` | `number \| undefined` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. |


# Example

```ts
import { AddSubnetRequest, Type42Enum } from 'hetzner-cloud-apilib';

const addSubnetRequest: AddSubnetRequest = {
  networkZone: 'eu-central',
  type: Type42Enum.Server,
  ipRange: '10.0.1.0/24',
  vswitchId: 1000,
};
```



