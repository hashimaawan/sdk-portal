# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Options2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `availableRegions` | `string[] \| undefined` | Optional | - |
| `subscriptionTiers` | [`SubscriptionTier[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/subscription-tier.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Options2 } from 'digitalocean-apilib';

const options2: Options2 = {
  availableRegions: [
    'nyc3'
  ],
  subscriptionTiers: [
    {
      allowStorageOverage: false,
      includedBandwidthBytes: BigInt(172),
      includedRepositories: 194,
      includedStorageBytes: BigInt(242),
      monthlyPriceInCents: 236,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      allowStorageOverage: false,
      includedBandwidthBytes: BigInt(172),
      includedRepositories: 194,
      includedStorageBytes: BigInt(242),
      monthlyPriceInCents: 236,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      allowStorageOverage: false,
      includedBandwidthBytes: BigInt(172),
      includedRepositories: 194,
      includedStorageBytes: BigInt(242),
      monthlyPriceInCents: 236,
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



