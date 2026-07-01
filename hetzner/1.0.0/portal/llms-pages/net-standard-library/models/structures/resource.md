# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc291cmNl


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Resource |
| `Type` | `string` | Required | Type of resource referenced |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Resource resource = new Resource
{
    Id = 42,
    Type = "server",
};
```



