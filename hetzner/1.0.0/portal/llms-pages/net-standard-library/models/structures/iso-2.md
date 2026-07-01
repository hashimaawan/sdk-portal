# Iso 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRklzbzI

ISO Image that is attached to this Server. Null if no ISO is attached.


# Class Name

`Iso2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Deprecated` | `string` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `Description` | `string` | Required | Description of the ISO |
| `Id` | `int` | Required | ID of the Resource |
| `Name` | `string` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `Type` | [`Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-26.md) | Required | Type of the ISO |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Iso2 iso2 = new Iso2
{
    Deprecated = "2018-02-28T00:00:00+00:00",
    Description = "FreeBSD 11.0 x64",
    Id = 42,
    Name = "FreeBSD-11.0-RELEASE-amd64-dvd1",
    Type = Type26Enum.Public,
};
```



