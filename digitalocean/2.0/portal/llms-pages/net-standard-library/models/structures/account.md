# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Account`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletLimit` | `int` | Required | The total number of Droplets current user or team may have active at one time. |
| `Email` | `string` | Required | The email address used by the current user to register for DigitalOcean. |
| `EmailVerified` | `bool` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `false` |
| `FloatingIpLimit` | `int` | Required | The total number of Floating IPs the current user or team may have. |
| `Status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `Status.active` |
| `StatusMessage` | `string` | Required | A human-readable message giving more details about the status of the account. |
| `Team` | [`Team`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. |
| `Uuid` | `string` | Required | The unique universal identifier for the current user. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Account account = new Account
{
    DropletLimit = 25,
    Email = "sammy@digitalocean.com",
    EmailVerified = true,
    FloatingIpLimit = 5,
    Status = Status.Active,
    StatusMessage = " ",
    Uuid = "b6fr89dbf6d9156cace5f3c78dc9851d957381ef",
    Team = new Team
    {
        Name = "name0",
        Uuid = "uuid6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



