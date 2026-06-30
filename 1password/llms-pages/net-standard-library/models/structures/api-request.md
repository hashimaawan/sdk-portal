# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type object.*


# Class Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/action.md) | Optional | - |
| `Actor` | [`Actor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/actor.md) | Optional | - |
| `RequestId` | `Guid?` | Optional | The unique id used to identify a single request. |
| `Resource` | [`Resource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/resource.md) | Optional | - |
| `Result` | [`Result?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/result.md) | Optional | - |
| `Timestamp` | `DateTime?` | Optional, Read-only | The time at which the request was processed by the server. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

ApiRequest apiRequest = new ApiRequest
{
    Action = Action.Read,
    Actor = new Actor
    {
        Account = "account0",
        Id = new Guid("0000193c-0000-0000-0000-000000000000"),
        Jti = "jti2",
        RequestIp = "requestIp4",
        UserAgent = "userAgent6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    RequestId = new Guid("000002a8-0000-0000-0000-000000000000"),
    Resource = new Resource
    {
        Item = new Item2
        {
            Id = "id2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ItemVersion = 108,
        Type = M1PasswordConnect.Standard.Models.Type.Item,
        Vault = new Vault3
        {
            Id = "id6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Result = Result.Success,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



