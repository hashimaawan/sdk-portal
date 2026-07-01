# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource

*This model accepts additional fields of type object.*


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Resource from being deleted |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Protection protection = new Protection
{
    Delete = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



