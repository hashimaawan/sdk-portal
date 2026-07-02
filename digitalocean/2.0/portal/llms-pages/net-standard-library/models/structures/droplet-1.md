# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Droplet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DestroyedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. |
| `ErrorMessage` | `string` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. |
| `Id` | `string` | Optional | The unique identifier for the resource scheduled for deletion. |
| `Name` | `string` | Optional | The name of the resource scheduled for deletion. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

Droplet1 droplet1 = new Droplet1
{
    DestroyedAt = DateTime.ParseExact("2020-04-01T18:11:49Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ErrorMessage = "error_message0",
    Id = "61486916",
    Name = "ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



