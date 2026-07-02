# Subscription

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvbg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Subscription`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | The time at which the subscription was created. |
| `tier` | [`Tier1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/tier-1.md) | Optional | - |
| `updatedAt` | `string \| undefined` | Optional, Read-only | The time at which the subscription was last updated. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Subscription } from 'digitalocean-apilib';

const subscription: Subscription = {
  createdAt: '2020-01-23T21:19:12Z',
  tier: {
    allowStorageOverage: false,
    includedBandwidthBytes: BigInt(46),
    includedRepositories: 68,
    includedStorageBytes: BigInt(112),
    monthlyPriceInCents: 110,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  updatedAt: '2020-11-05T15:53:24Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



