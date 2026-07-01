# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerTypes` | [`List<ServerTypes7>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-types-7.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServerTypesResponse serverTypesResponse = new ServerTypesResponse
{
    ServerTypes = new List<ServerTypes7>
    {
        new ServerTypes7
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
    },
};
```



