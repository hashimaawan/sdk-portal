# Iso

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRklzbw

*This model accepts additional fields of type unknown.*


# Interface Name

`Iso`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `string \| null` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `description` | `string` | Required | Description of the ISO |
| `id` | `number` | Required | ID of the Resource |
| `name` | `string \| null` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `type` | [`Type26`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-26.md) | Required | Type of the ISO |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Iso, Type26 } from 'hetzner-cloud-apilib';

const iso: Iso = {
  deprecated: '2018-02-28T00:00:00+00:00',
  description: 'FreeBSD 11.0 x64',
  id: 42,
  name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
  type: Type26.Public,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



