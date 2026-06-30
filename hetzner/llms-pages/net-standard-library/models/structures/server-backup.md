# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Percentage` | `string` | Required | Percentage by how much the base price will increase |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ServerBackup serverBackup = new ServerBackup
{
    Percentage = "20.0000000000",
};
```



