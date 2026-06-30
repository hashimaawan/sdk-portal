# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Interface Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/iso.md) | Required | - |


# Example

```ts
import { IsosResponse1, Type26Enum } from 'hetzner-cloud-apilib';

const isosResponse1: IsosResponse1 = {
  iso: {
    deprecated: '2018-02-28T00:00:00+00:00',
    description: 'FreeBSD 11.0 x64',
    id: 42,
    name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
    type: Type26Enum.Public,
  },
};
```



