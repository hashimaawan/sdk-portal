# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ


# Interface Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `serverType` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-type.md) | Required | - |


# Example

```ts
import {
  CpuTypeEnum,
  ServerTypesResponse1,
  StorageTypeEnum,
} from 'hetzner-cloud-apilib';

const serverTypesResponse1: ServerTypesResponse1 = {
  serverType: {
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
  },
};
```



