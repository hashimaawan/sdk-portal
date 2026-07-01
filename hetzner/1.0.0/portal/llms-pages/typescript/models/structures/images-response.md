# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `images` | [`Image[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/image.md) | Required | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ImagesResponse,
  OsFlavor,
  Status24,
  Type22,
} from 'hetzner-cloud-apilib';

const imagesResponse: ImagesResponse = {
  images: [
    {
      boundTo: null,
      created: '2016-01-30T23:55:00+00:00',
      createdFrom: {
        id: 1,
        name: 'Server',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      deleted: null,
      deprecated: '2018-02-28T00:00:00+00:00',
      description: 'Ubuntu 20.04 Standard 64 bit',
      diskSize: 10,
      id: 42,
      imageSize: 2.3,
      labels: {
        'key0': 'labels0',
        'key1': 'labels1'
      },
      name: 'ubuntu-20.04',
      osFlavor: OsFlavor.Ubuntu,
      osVersion: '20.04',
      protection: {
        mDelete: false,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      status: Status24.Available,
      type: Type22.Snapshot,
      rapidDeploy: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  meta: {
    pagination: {
      lastPage: 77.7,
      nextPage: 209.18,
      page: 17.58,
      perPage: 13.34,
      previousPage: 50.02,
      totalEntries: 206.64,
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



