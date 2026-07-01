# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type object.*


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/location.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LocationsResponse1 locationsResponse1 = new LocationsResponse1
{
    Location = new Location
    {
        City = "Falkenstein",
        Country = "DE",
        Description = "Falkenstein DC Park 1",
        Id = 1,
        Latitude = 50.47612,
        Longitude = 12.370071,
        Name = "fsn1",
        NetworkZone = "eu-central",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



