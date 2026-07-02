# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `continent` | `string \| undefined` | Optional, Read-only | - |
| `dataCenters` | `string[] \| undefined` | Optional, Read-only | - |
| `mDefault` | `boolean \| undefined` | Optional, Read-only | Whether or not the region is presented as the default. |
| `disabled` | `boolean \| undefined` | Optional, Read-only | - |
| `flag` | `string \| undefined` | Optional, Read-only | - |
| `label` | `string \| undefined` | Optional, Read-only | - |
| `reason` | `string \| undefined` | Optional, Read-only | - |
| `slug` | `string \| undefined` | Optional, Read-only | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { GeographicalInformationAboutAnAppOrigin } from 'digitalocean-apilib';

const geographicalInformationAboutAnAppOrigin: GeographicalInformationAboutAnAppOrigin = {
  continent: 'europe',
  dataCenters: [
    'ams'
  ],
  mDefault: true,
  disabled: true,
  flag: 'ams',
  label: 'ams',
  reason: 'to crowded',
  slug: 'basic',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



