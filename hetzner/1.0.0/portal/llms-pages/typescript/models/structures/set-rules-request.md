# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rules` | [`Rule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Direction, Protocol, SetRulesRequest } from 'hetzner-cloud-apilib';

const setRulesRequest: SetRulesRequest = {
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



