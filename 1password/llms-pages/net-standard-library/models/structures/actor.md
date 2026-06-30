# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type object.*


# Class Name

`Actor`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Account` | `string` | Optional | - |
| `Id` | `Guid?` | Optional | - |
| `Jti` | `string` | Optional | - |
| `RequestIp` | `string` | Optional | - |
| `UserAgent` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Actor actor = new Actor
{
    Account = "account0",
    Id = new Guid("0000193c-0000-0000-0000-000000000000"),
    Jti = "jti2",
    RequestIp = "requestIp4",
    UserAgent = "userAgent6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



