# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tiers` | [`Tier[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/tier.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsTiersResponse } from 'digitalocean-apilib';

const v2AppsTiersResponse: V2AppsTiersResponse = {
  tiers: [
    {
      buildSeconds: 'build_seconds4',
      egressBandwidthBytes: 'egress_bandwidth_bytes2',
      name: 'name8',
      slug: 'slug8',
      storageBytes: 'storage_bytes4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      buildSeconds: 'build_seconds4',
      egressBandwidthBytes: 'egress_bandwidth_bytes2',
      name: 'name8',
      slug: 'slug8',
      storageBytes: 'storage_bytes4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      buildSeconds: 'build_seconds4',
      egressBandwidthBytes: 'egress_bandwidth_bytes2',
      name: 'name8',
      slug: 'slug8',
      storageBytes: 'storage_bytes4',
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



