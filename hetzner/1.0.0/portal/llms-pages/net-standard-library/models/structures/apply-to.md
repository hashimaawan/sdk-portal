# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGx5VG8

*This model accepts additional fields of type object.*


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `Server` | [`Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `Type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-7.md) | Required | Type of the resource |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

ApplyTo applyTo = new ApplyTo
{
    Type = Type7.Server,
    LabelSelector = new LabelSelector1
    {
        Selector = "selector8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Server = new Server2
    {
        Id = 14,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



