# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type unknown.*


# Interface Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/iso.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { IsosResponse1, Type26 } from 'hetzner-cloud-apilib';

const isosResponse1: IsosResponse1 = {
  iso: {
    deprecated: '2018-02-28T00:00:00+00:00',
    description: 'FreeBSD 11.0 x64',
    id: 42,
    name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
    type: Type26.Public,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



