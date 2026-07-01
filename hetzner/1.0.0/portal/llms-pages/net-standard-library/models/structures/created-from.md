# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from

*This model accepts additional fields of type object.*


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server the Image was created from |
| `Name` | `string` | Required | Server name at the time the Image was created |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

CreatedFrom createdFrom = new CreatedFrom
{
    Id = 1,
    Name = "Server",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



