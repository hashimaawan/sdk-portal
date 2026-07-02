# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Alert`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Disabled` | `bool?` | Optional | Is the alert disabled? |
| `Operator` | [`Operator?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/operator.md) | Optional | **Default**: `Operator.UNSPECIFIED_OPERATOR` |
| `Rule` | [`Rule?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/rule.md) | Optional | **Default**: `Rule.UNSPECIFIED_RULE` |
| `MValue` | `double?` | Optional | Threshold value for alert |
| `Window` | [`Window?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/window.md) | Optional | **Default**: `Window.UNSPECIFIED_WINDOW` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Alert alert = new Alert
{
    Disabled = false,
    MOperator = Operator.GreaterThan,
    Rule = Rule.CpuUtilization,
    MValue = 2.32,
    Window = Window.FiveMinutes,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



