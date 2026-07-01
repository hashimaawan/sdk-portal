# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/location.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

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
    },
};
```



