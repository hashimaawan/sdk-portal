# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

An objects containing information about a resource associated with a Droplet.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cost` | `string` | Optional | The cost of the resource in USD per month if the resource is retained after the Droplet is destroyed. |
| `Id` | `string` | Optional | The unique identifier for the resource associated with the Droplet. |
| `Name` | `string` | Optional | The name of the resource associated with the Droplet. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

FloatingIp floatingIp = new FloatingIp
{
    Cost = "0.05",
    Id = "61486916",
    Name = "ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



