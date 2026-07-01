# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Interface Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `images` | [`Image[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/image.md) | Required | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |


# Example

```ts
import {
  ImagesResponse,
  OsFlavorEnum,
  Status24Enum,
  Type22Enum,
} from 'hetzner-cloud-apilib';

const imagesResponse: ImagesResponse = {
  images: [
    {
      boundTo: null,
      created: '2016-01-30T23:55:00+00:00',
      createdFrom: {
        id: 1,
        name: 'Server',
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
      osFlavor: OsFlavorEnum.Ubuntu,
      osVersion: '20.04',
      protection: {
        mDelete: false,
      },
      status: Status24Enum.Available,
      type: Type22Enum.Snapshot,
      rapidDeploy: false,
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
    },
  },
};
```



