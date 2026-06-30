# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Interface Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/image.md) | Optional | - |


# Example

```ts
import {
  ImagesResponse1,
  OsFlavorEnum,
  Status24Enum,
  Type22Enum,
} from 'hetzner-cloud-apilib';

const imagesResponse1: ImagesResponse1 = {
  image: {
    boundTo: 186,
    created: 'created6',
    createdFrom: {
      id: 60,
      name: 'name6',
    },
    deleted: 'deleted4',
    deprecated: 'deprecated8',
    description: 'description6',
    diskSize: 244.18,
    id: 128,
    imageSize: 141.34,
    labels: {
      'key0': 'labels4'
    },
    name: 'name6',
    osFlavor: OsFlavorEnum.Debian,
    osVersion: 'os_version4',
    protection: {
      mDelete: false,
    },
    status: Status24Enum.Unavailable,
    type: Type22Enum.App,
    rapidDeploy: false,
  },
};
```



