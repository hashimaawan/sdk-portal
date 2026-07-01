# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/iso.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

IsosResponse1 isosResponse1 = new IsosResponse1
{
    Iso = new Iso
    {
        Deprecated = "2018-02-28T00:00:00+00:00",
        Description = "FreeBSD 11.0 x64",
        Id = 42,
        Name = "FreeBSD-11.0-RELEASE-amd64-dvd1",
        Type = Type26Enum.Public,
    },
};
```



