# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type unknown.*


# Interface Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ImagesResponse1,
  OsFlavor,
  Status24,
  Type22,
} from 'hetzner-cloud-apilib';

const imagesResponse1: ImagesResponse1 = {
  image: {
    boundTo: 186,
    created: 'created6',
    createdFrom: {
      id: 60,
      name: 'name6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
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
    osFlavor: OsFlavor.Debian,
    osVersion: 'os_version4',
    protection: {
      mDelete: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    status: Status24.Unavailable,
    type: Type22.App,
    rapidDeploy: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



