# V2 Apps Alerts Destinations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alert` | [`Alert1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/alert-1.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2AppsAlertsDestinationsResponse v2AppsAlertsDestinationsResponse = new V2AppsAlertsDestinationsResponse
{
    Alert = new Alert1
    {
        ComponentName = "component_name2",
        Emails = new List<string>
        {
            "emails9",
        },
        Id = "id0",
        Phase = Phase1.Configuring,
        Progress = new Progress2
        {
            Steps = new List<StepsOfAnAlertSProgress>
            {
                new StepsOfAnAlertSProgress
                {
                    EndedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                        provider: CultureInfo.InvariantCulture,
                        DateTimeStyles.RoundtripKind),
                    Name = "name2",
                    Reason = new Reason
                    {
                        Code = "code2",
                        Message = "message4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    StartedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                        provider: CultureInfo.InvariantCulture,
                        DateTimeStyles.RoundtripKind),
                    Status = Status2.Success,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new StepsOfAnAlertSProgress
                {
                    EndedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                        provider: CultureInfo.InvariantCulture,
                        DateTimeStyles.RoundtripKind),
                    Name = "name2",
                    Reason = new Reason
                    {
                        Code = "code2",
                        Message = "message4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    StartedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                        provider: CultureInfo.InvariantCulture,
                        DateTimeStyles.RoundtripKind),
                    Status = Status2.Success,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new StepsOfAnAlertSProgress
                {
                    EndedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                        provider: CultureInfo.InvariantCulture,
                        DateTimeStyles.RoundtripKind),
                    Name = "name2",
                    Reason = new Reason
                    {
                        Code = "code2",
                        Message = "message4",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    StartedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                        provider: CultureInfo.InvariantCulture,
                        DateTimeStyles.RoundtripKind),
                    Status = Status2.Success,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



