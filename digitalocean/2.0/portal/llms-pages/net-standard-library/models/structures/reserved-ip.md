# Reserved Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc2VydmVkSXA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ReservedIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Droplet` | [`ReservedIpDroplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/reserved-ip-droplet.md) | Optional | This is a container for any-of cases. |
| `Ip` | `string` | Optional | The public IP address of the reserved IP. It also serves as its identifier. |
| `Locked` | `bool?` | Optional | A boolean value indicating whether or not the reserved IP has pending actions preventing new ones from being submitted. |
| `ProjectId` | `Guid?` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/region.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

ReservedIp reservedIp = new ReservedIp
{
    Droplet = ReservedIpDroplet.FromObject(
        ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ),
    Ip = "45.55.96.47",
    Locked = true,
    ProjectId = new Guid("746c6152-2fa2-11ed-92d3-27aaa54e4988"),
    Region = new Region
    {
        Available = false,
        Features = new List<string>
        {
            "features7",
            "features8",
            "features9",
        },
        Name = "name6",
        Sizes = new List<string>
        {
            "sizes6",
        },
        Slug = "slug0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



