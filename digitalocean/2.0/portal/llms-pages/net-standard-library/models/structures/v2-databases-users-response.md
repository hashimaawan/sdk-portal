# V2 Databases Users Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Users` | [`List<User>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/user.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2DatabasesUsersResponse v2DatabasesUsersResponse = new V2DatabasesUsersResponse
{
    Users = new List<User>
    {
        new User
        {
            Name = "name6",
            MysqlSettings = new MysqlSettings
            {
                AuthPlugin = AuthPlugin.MysqlNativePassword,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Password = "password0",
            Role = Role.Primary,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new User
        {
            Name = "name6",
            MysqlSettings = new MysqlSettings
            {
                AuthPlugin = AuthPlugin.MysqlNativePassword,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Password = "password0",
            Role = Role.Primary,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



