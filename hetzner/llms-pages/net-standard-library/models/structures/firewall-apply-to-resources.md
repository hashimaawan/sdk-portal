# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw


# Class Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `Server` | [`Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `Type` | [`Type7Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-7.md) | Optional | Type of the resource |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

FirewallApplyToResources firewallApplyToResources = new FirewallApplyToResources
{
    LabelSelector = new LabelSelector5
    {
        Selector = "selector8",
    },
    Server = new Server9
    {
        Id = 14,
    },
    Type = Type7Enum.Server,
};
```



