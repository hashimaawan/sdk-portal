# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CheckName` | `string` | Optional | The clusterlint check that resulted in the diagnostic. |
| `Message` | `string` | Optional | Feedback about the object for users to fix. |
| `MObject` | [`MObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. |
| `Severity` | `string` | Optional | Can be one of error, warning or suggestion. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Diagnostic diagnostic = new Diagnostic
{
    CheckName = "unused-config-map",
    Message = "Unused config map",
    MObject = new MObject
    {
        Kind = "kind0",
        Name = "name2",
        MNamespace = "namespace0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Severity = "warning",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



