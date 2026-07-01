# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGx5VG8


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `Server` | [`Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `Type` | [`Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-7.md) | Required | Type of the resource |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ApplyTo applyTo = new ApplyTo
{
    Type = Type7Enum.Server,
    LabelSelector = new LabelSelector1
    {
        Selector = "selector8",
    },
    Server = new Server2
    {
        Id = 14,
    },
};
```



