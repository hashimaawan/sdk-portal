# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `serverTypes` | [`ServerTypes7[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-types-7.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CpuType,
  ServerTypesResponse,
  StorageType,
} from 'hetzner-cloud-apilib';

const serverTypesResponse: ServerTypesResponse = {
  serverTypes: [
    {
      cores: 1,
      cpuType: CpuType.Shared,
      deprecated: false,
      description: 'CX11',
      disk: 24,
      id: 1,
      memory: 1,
      name: 'cx11',
      prices: [
        {
          location: 'fsn1',
          priceHourly: {
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          priceMonthly: {
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      storageType: StorageType.Local,
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



