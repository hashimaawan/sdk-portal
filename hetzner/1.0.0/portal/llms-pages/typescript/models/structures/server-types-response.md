# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Interface Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `serverTypes` | [`ServerTypes7[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-types-7.md) | Required | - |


# Example

```ts
import {
  CpuTypeEnum,
  ServerTypesResponse,
  StorageTypeEnum,
} from 'hetzner-cloud-apilib';

const serverTypesResponse: ServerTypesResponse = {
  serverTypes: [
    {
      cores: 1,
      cpuType: CpuTypeEnum.Shared,
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
          },
          priceMonthly: {
            gross: '1.1900000000000000',
            net: '1.0000000000',
          },
        }
      ],
      storageType: StorageTypeEnum.Local,
    }
  ],
};
```



