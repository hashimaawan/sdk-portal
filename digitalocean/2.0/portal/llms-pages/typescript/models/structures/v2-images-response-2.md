# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/image-1.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Distribution,
  Region2,
  Status7,
  Type9,
  V2ImagesResponse2,
} from 'digitalocean-apilib';

const v2ImagesResponse2: V2ImagesResponse2 = {
  image: {
    createdAt: '2020-05-04T22:23:02Z',
    description: 'description6',
    distribution: Distribution.Ubuntu,
    errorMessage: 'error_message8',
    id: 7555620,
    minDiskSize: 20,
    name: 'Nifty New Snapshot',
    mPublic: true,
    regions: [
      Region2.Nyc1,
      Region2.Nyc2
    ],
    sizeGigabytes: 2.34,
    slug: 'nifty1',
    status: Status7.New,
    tags: [
      'base-image',
      'prod'
    ],
    type: Type9.Snapshot,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



