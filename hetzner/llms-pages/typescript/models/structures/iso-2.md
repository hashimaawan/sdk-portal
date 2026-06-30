# Iso 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRklzbzI

ISO Image that is attached to this Server. Null if no ISO is attached.


# Interface Name

`Iso2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `string \| null` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `description` | `string` | Required | Description of the ISO |
| `id` | `number` | Required | ID of the Resource |
| `name` | `string \| null` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `type` | [`Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-26.md) | Required | Type of the ISO |


# Example

```ts
import { Iso2, Type26Enum } from 'hetzner-cloud-apilib';

const iso2: Iso2 = {
  deprecated: '2018-02-28T00:00:00+00:00',
  description: 'FreeBSD 11.0 x64',
  id: 42,
  name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
  type: Type26Enum.Public,
};
```



