# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `inboundRules` | [`InboundRule[] \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/inbound-rule.md) | Required | - |
| `outboundRules` | [`OutboundRule[] \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/outbound-rule.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Protocol, V2FirewallsRulesRequest } from 'digitalocean-apilib';

const v2FirewallsRulesRequest: V2FirewallsRulesRequest = {
  inboundRules: [
    {
      ports: '8000',
      protocol: Protocol.Tcp,
      sources: {
        addresses: [
          '1.2.3.4',
          '18.0.0.0/8'
        ],
        dropletIds: [
          8043964
        ],
        kubernetesIds: [
          '41b74c5d-9bd0-5555-5555-a57c495b81a3'
        ],
        loadBalancerUids: [
          '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ],
        tags: [
          'tags1',
          'tags2',
          'tags3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  outboundRules: [
    {
      ports: '8000',
      protocol: Protocol.Tcp,
      destinations: {
        addresses: [
          '1.2.3.4',
          '18.0.0.0/8'
        ],
        dropletIds: [
          8043964
        ],
        kubernetesIds: [
          '41b74c5d-9bd0-5555-5555-a57c495b81a3'
        ],
        loadBalancerUids: [
          '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ],
        tags: [
          'tags7',
          'tags8',
          'tags9'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
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



