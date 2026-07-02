# V2 Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBTaXplcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2SizesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sizes` | [`Size[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/size.md) | Required | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2SizesResponse } from 'digitalocean-apilib';

const v2SizesResponse: V2SizesResponse = {
  sizes: [
    {
      available: true,
      description: 'Basic',
      disk: 25,
      memory: 1024,
      priceHourly: 0.00743999984115362,
      priceMonthly: 5,
      regions: [
        'ams2',
        'ams3',
        'blr1',
        'fra1',
        'lon1',
        'nyc1',
        'nyc2',
        'nyc3',
        'sfo1',
        'sfo2',
        'sfo3',
        'sgp1',
        'tor1'
      ],
      slug: 's-1vcpu-1gb',
      transfer: 1,
      vcpus: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  meta: {
    total: 64,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  links: {
    pages: {
      last: 'https://api.digitalocean.com/v2/sizes?page=64&per_page=1',
      next: 'https://api.digitalocean.com/v2/sizes?page=2&per_page=1',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



