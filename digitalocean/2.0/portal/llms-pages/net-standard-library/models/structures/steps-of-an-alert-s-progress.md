# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EndedAt` | `DateTime?` | Optional | - |
| `Name` | `string` | Optional | - |
| `Reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/reason.md) | Optional | - |
| `StartedAt` | `DateTime?` | Optional | - |
| `Status` | [`Status2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-2.md) | Optional | **Default**: `Status2.UNKNOWN` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

StepsOfAnAlertSProgress stepsOfAnAlertSProgress = new StepsOfAnAlertSProgress
{
    EndedAt = DateTime.ParseExact("2020-11-19T20:27:18Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Name = "example_step",
    Reason = new Reason
    {
        Code = "code2",
        Message = "message4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    StartedAt = DateTime.ParseExact("2020-11-19T20:27:18Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Status = Status2.Success,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



