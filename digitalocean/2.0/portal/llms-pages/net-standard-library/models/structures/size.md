# Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNpemU

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Size`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Available` | `bool` | Required | This is a boolean value that represents whether new Droplets can be created with this size.<br><br>**Default**: `true` |
| `Description` | `string` | Required | A string describing the class of Droplets created from this size. For example: Basic, General Purpose, CPU-Optimized, Memory-Optimized, or Storage-Optimized. |
| `Disk` | `int` | Required | The amount of disk space set aside for Droplets of this size. The value is represented in gigabytes. |
| `Memory` | `int` | Required | The amount of RAM allocated to Droplets created of this size. The value is represented in megabytes.<br><br>**Constraints**: `>= 8`, *Multiple Of*: `8` |
| `PriceHourly` | `double` | Required | This describes the price of the Droplet size as measured hourly. The value is measured in US dollars. |
| `PriceMonthly` | `double` | Required | This attribute describes the monthly cost of this Droplet size if the Droplet is kept for an entire month. The value is measured in US dollars. |
| `Regions` | `List<string>` | Required | An array containing the region slugs where this size is available for Droplet creates. |
| `Slug` | `string` | Required | A human-readable string that is used to uniquely identify each size. |
| `Transfer` | `double` | Required | The amount of transfer bandwidth that is available for Droplets created in this size. This only counts traffic on the public interface. The value is given in terabytes. |
| `Vcpus` | `int` | Required | The integer of number CPUs allocated to Droplets of this size. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Size size = new Size
{
    Available = true,
    Description = "Basic",
    Disk = 25,
    Memory = 1024,
    PriceHourly = 0.00743999984115362,
    PriceMonthly = 5,
    Regions = new List<string>
    {
        "ams2",
        "ams3",
        "blr1",
        "fra1",
        "lon1",
        "nyc1",
        "nyc2",
        "nyc3",
        "sfo1",
        "sfo2",
        "sfo3",
        "sgp1",
        "tor1",
    },
    Slug = "s-1vcpu-1gb",
    Transfer = 1,
    Vcpus = 1,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



