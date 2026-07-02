# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `options` | [`Options2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/options-2.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2RegistryOptionsResponse } from 'digitalocean-apilib';

const v2RegistryOptionsResponse: V2RegistryOptionsResponse = {
  options: {
    availableRegions: [
      'available_regions9'
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
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



