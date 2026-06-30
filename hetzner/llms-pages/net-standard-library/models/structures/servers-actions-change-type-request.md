# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | `string` | Required | ID or name of Server type the Server should migrate to |
| `UpgradeDisk` | `bool` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ServersActionsChangeTypeRequest serversActionsChangeTypeRequest = new ServersActionsChangeTypeRequest
{
    ServerType = "cx11",
    UpgradeDisk = true,
};
```



