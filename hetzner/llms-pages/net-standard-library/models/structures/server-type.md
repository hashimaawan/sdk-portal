# Server Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlclR5cGU


# Class Name

`ServerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cores` | `double` | Required | Number of cpu cores a Server of this type will have |
| `CpuType` | [`CpuTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `Deprecated` | `bool` | Required | True if Server type is deprecated |
| `Description` | `string` | Required | Description of the Server type |
| `Disk` | `double` | Required | Disk size a Server of this type will have in GB |
| `Id` | `double` | Required | ID of the Server type |
| `Memory` | `double` | Required | Memory a Server of this type will have in GB |
| `Name` | `string` | Required | Unique identifier of the Server type |
| `Prices` | [`List<Price9>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-9.md) | Required | Prices in different Locations |
| `StorageType` | [`StorageTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServerType serverType = new ServerType
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
};
```



