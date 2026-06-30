# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA


# Interface Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applyTo` | [`ApplyTo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Firewall |
| `rules` | [`Rule[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/rule.md) | Optional | Array of rules |


# Example

```ts
import {
  CreateFirewallRequest,
  DirectionEnum,
  ProtocolEnum,
  Type7Enum,
} from 'hetzner-cloud-apilib';

const createFirewallRequest: CreateFirewallRequest = {
  name: 'Corporate Intranet Protection',
  applyTo: [
    {
      type: Type7Enum.Server,
      labelSelector: {
        selector: 'selector8',
      },
      server: {
        id: 14,
      },
    },
    {
      type: Type7Enum.Server,
      labelSelector: {
        selector: 'selector8',
      },
      server: {
        id: 14,
      },
    },
    {
      type: Type7Enum.Server,
      labelSelector: {
        selector: 'selector8',
      },
      server: {
        id: 14,
      },
    }
  ],
  labels: { 'key1': 'val1', 'key2': 'val2' },
  rules: [
    {
      direction: DirectionEnum.In,
      protocol: ProtocolEnum.Tcp,
      description: 'description2',
      destinationIps: [
        'destination_ips1',
        'destination_ips2',
        'destination_ips3'
      ],
      port: '80',
      sourceIps: [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
      ],
    }
  ],
};
```



