# V2 Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancer` | [`LoadBalancer1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/load-balancer-1.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Algorithm,
  EntryProtocol,
  TargetProtocol,
  V2LoadBalancersResponse1,
} from 'digitalocean-apilib';

const v2LoadBalancersResponse1: V2LoadBalancersResponse1 = {
  loadBalancer: {
    forwardingRules: [
      {
        entryPort: 220,
        entryProtocol: EntryProtocol.Http2,
        targetPort: 104,
        targetProtocol: TargetProtocol.Https,
        certificateId: 'certificate_id4',
        tlsPassthrough: false,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        entryPort: 220,
        entryProtocol: EntryProtocol.Http2,
        targetPort: 104,
        targetProtocol: TargetProtocol.Https,
        certificateId: 'certificate_id4',
        tlsPassthrough: false,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    algorithm: Algorithm.RoundRobin,
    createdAt: '2016-03-13T12:52:32.123Z',
    disableLetsEncryptDnsRecords: false,
    enableBackendKeepalive: false,
    enableProxyProtocol: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



