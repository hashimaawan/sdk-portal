# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `forwardingRules` | [`ForwardingRule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  EntryProtocol,
  TargetProtocol,
  V2LoadBalancersForwardingRulesRequest,
} from 'digitalocean-apilib';

const v2LoadBalancersForwardingRulesRequest: V2LoadBalancersForwardingRulesRequest = {
  forwardingRules: [
    {
      entryPort: 443,
      entryProtocol: EntryProtocol.Https,
      targetPort: 80,
      targetProtocol: TargetProtocol.Http,
      certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
      tlsPassthrough: false,
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



