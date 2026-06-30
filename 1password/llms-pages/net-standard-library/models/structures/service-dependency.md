# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type object.*


# Class Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Message` | `string` | Optional | Human-readable message for explaining the current state. |
| `Service` | `string` | Optional | - |
| `Status` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

ServiceDependency serviceDependency = new ServiceDependency
{
    Message = "message6",
    Service = "service6",
    Status = "status8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



