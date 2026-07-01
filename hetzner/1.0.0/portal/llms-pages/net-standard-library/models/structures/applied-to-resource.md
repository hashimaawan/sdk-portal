# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl

*This model accepts additional fields of type object.*


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server.md) | Optional | - |
| `Type` | [`Type5?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-5.md) | Optional | Type of resource referenced |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

AppliedToResource appliedToResource = new AppliedToResource
{
    Server = new Server
    {
        Id = 14,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Type = Type5.Server,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



