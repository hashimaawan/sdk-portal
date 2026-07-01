# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJ1bGU

*This model accepts additional fields of type unknown.*


# Interface Name

`Rule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| null \| undefined` | Optional | Description of the Rule<br><br>**Constraints**: *Maximum Length*: `255` |
| `destinationIps` | `string[] \| undefined` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. |
| `direction` | [`Direction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/direction.md) | Required | Select traffic direction on which rule should be applied. Use `source_ips` for direction `in` and `destination_ips` for direction `out`. |
| `port` | `string \| undefined` | Optional | Port or port range to which traffic will be allowed, only applicable for protocols TCP and UDP. A port range can be specified by separating two ports with a dash, e.g `1024-5000`. |
| `protocol` | [`Protocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/protocol.md) | Required | Type of traffic to allow |
| `sourceIps` | `string[] \| undefined` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Direction, Protocol, Rule } from 'hetzner-cloud-apilib';

const rule: Rule = {
  direction: Direction.In,
  protocol: Protocol.Esp,
  description: 'description0',
  destinationIps: [
    '28.239.13.1/32',
    '28.239.14.0/24',
    'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
  ],
  port: '80',
  sourceIps: [
    '28.239.13.1/32',
    '28.239.14.0/24',
    'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



