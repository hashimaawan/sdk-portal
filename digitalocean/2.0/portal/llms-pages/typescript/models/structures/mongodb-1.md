# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endOfAvailability` | `string \| undefined` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `endOfLife` | `string \| undefined` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `version` | `string \| undefined` | Optional | The engine version. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Mongodb1 } from 'digitalocean-apilib';

const mongodb1: Mongodb1 = {
  endOfAvailability: '2023-05-09T00:00:00Z',
  endOfLife: '2023-11-09T00:00:00Z',
  version: '8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



