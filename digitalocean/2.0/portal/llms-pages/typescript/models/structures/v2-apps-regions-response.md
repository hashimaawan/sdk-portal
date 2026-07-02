# V2 Apps Regions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZWdpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsRegionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | [`GeographicalInformationAboutAnAppOrigin[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsRegionsResponse } from 'digitalocean-apilib';

const v2AppsRegionsResponse: V2AppsRegionsResponse = {
  regions: [
    {
      continent: 'continent2',
      dataCenters: [
        'data_centers9'
      ],
      mDefault: false,
      disabled: false,
      flag: 'flag4',
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



