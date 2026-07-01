# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server the Image was created from |
| `Name` | `string` | Required | Server name at the time the Image was created |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

CreatedFrom createdFrom = new CreatedFrom
{
    Id = 1,
    Name = "Server",
};
```



