# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Tier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `buildSeconds` | `string \| undefined` | Optional | - |
| `egressBandwidthBytes` | `string \| undefined` | Optional | - |
| `name` | `string \| undefined` | Optional | - |
| `slug` | `string \| undefined` | Optional | - |
| `storageBytes` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Tier } from 'digitalocean-apilib';

const tier: Tier = {
  buildSeconds: '233',
  egressBandwidthBytes: '123',
  name: 'test',
  slug: 'test',
  storageBytes: '10000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



