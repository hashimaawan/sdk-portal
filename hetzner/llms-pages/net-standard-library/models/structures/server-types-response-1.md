# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/server-type.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServerTypesResponse1 serverTypesResponse1 = new ServerTypesResponse1
{
    ServerType = new ServerType
    {
        Cores = 1,
        CpuType = CpuTypeEnum.Shared,
        Deprecated = false,
        Description = "CX11",
        Disk = 24,
        Id = 1,
        Memory = 1,
        Name = "cx11",
        Prices = new List<Price9>
        {
            new Price9
            {
                Location = "fsn1",
                PriceHourly = new PriceHourly8
                {
                    Gross = "1.1900000000000000",
                    Net = "1.0000000000",
                },
                PriceMonthly = new PriceMonthly10
                {
                    Gross = "1.1900000000000000",
                    Net = "1.0000000000",
                },
            },
        },
        StorageType = StorageTypeEnum.Local,
    },
};
```



