# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type unknown.*


# Interface Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appliedTo` | [`AppliedTo[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/applied-to.md) | Required | - |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `number` | Required | ID of the Resource |
| `labels` | `Record<string, string> \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `rules` | [`Rule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/rule.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  Direction,
  Firewall,
  Protocol,
  Type5,
  Type6,
} from 'hetzner-cloud-apilib';

const firewall: Firewall = {
  appliedTo: [
    {
      type: Type6.Server,
      appliedToResources: [
        {
          server: {
            id: 14,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          type: Type5.Server,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
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
  created: '2016-01-30T23:55:00+00:00',
  id: 42,
  name: 'my-resource',
  rules: [
    {
      direction: Direction.In,
      protocol: Protocol.Udp,
      description: 'description2',
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
    }
  ],
  labels: {
    'key0': 'labels2',
    'key1': 'labels1'
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



