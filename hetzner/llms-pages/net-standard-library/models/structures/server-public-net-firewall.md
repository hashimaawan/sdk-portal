# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int?` | Optional | ID of the Resource |
| `Status` | [`Status72Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ServerPublicNetFirewall serverPublicNetFirewall = new ServerPublicNetFirewall
{
    Id = 42,
    Status = Status72Enum.Applied,
};
```



