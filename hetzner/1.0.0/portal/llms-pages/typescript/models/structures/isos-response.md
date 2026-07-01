# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isos` | [`Iso[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/iso.md) | Required | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { IsosResponse, Type26 } from 'hetzner-cloud-apilib';

const isosResponse: IsosResponse = {
  isos: [
    {
      deprecated: '2018-02-28T00:00:00+00:00',
      description: 'FreeBSD 11.0 x64',
      id: 42,
      name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
      type: Type26.Public,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  meta: {
    pagination: {
      lastPage: 77.7,
      nextPage: 209.18,
      page: 17.58,
      perPage: 13.34,
      previousPage: 50.02,
      totalEntries: 206.64,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



