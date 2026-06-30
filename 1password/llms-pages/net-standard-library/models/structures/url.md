# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type object.*


# Class Name

`Url`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | - |
| `Label` | `string` | Optional | - |
| `Primary` | `bool?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Url url = new Url
{
    Href = "href6",
    Label = "label4",
    Primary = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



