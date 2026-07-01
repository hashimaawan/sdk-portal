# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applyTo` | [`ApplyTo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Firewall |
| `rules` | [`Rule[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/rule.md) | Optional | Array of rules |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CreateFirewallRequest,
  Direction,
  Protocol,
  Type7,
} from 'hetzner-cloud-apilib';

const createFirewallRequest: CreateFirewallRequest = {
  name: 'Corporate Intranet Protection',
  applyTo: [
    {
      type: Type7.Server,
      labelSelector: {
        selector: 'selector8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      server: {
        id: 14,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      type: Type7.Server,
      labelSelector: {
        selector: 'selector8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      server: {
        id: 14,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      type: Type7.Server,
      labelSelector: {
        selector: 'selector8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      server: {
        id: 14,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  labels: { 'key1': 'val1', 'key2': 'val2' },
  rules: [
    {
      direction: Direction.In,
      protocol: Protocol.Tcp,
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
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



