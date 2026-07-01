# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw

*This model accepts additional fields of type object.*


# Class Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `Server` | [`Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `Type` | [`Type7?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-7.md) | Optional | Type of the resource |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

FirewallApplyToResources firewallApplyToResources = new FirewallApplyToResources
{
    LabelSelector = new LabelSelector5
    {
        Selector = "selector8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Server = new Server9
    {
        Id = 14,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Type = Type7.Server,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



