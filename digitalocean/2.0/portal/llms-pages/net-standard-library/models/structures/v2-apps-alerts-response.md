# V2 Apps Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsAlertsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alerts` | [`List<Alert1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/alert-1.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2AppsAlertsResponse v2AppsAlertsResponse = new V2AppsAlertsResponse
{
    Alerts = new List<Alert1>
    {
        new Alert1
        {
            ComponentName = "component_name6",
            Emails = new List<string>
            {
                "emails5",
                "emails6",
            },
            Id = "id6",
            Phase = Phase1.Active,
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
        new Alert1
        {
            ComponentName = "component_name6",
            Emails = new List<string>
            {
                "emails5",
                "emails6",
            },
            Id = "id6",
            Phase = Phase1.Active,
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
        new Alert1
        {
            ComponentName = "component_name6",
            Emails = new List<string>
            {
                "emails5",
                "emails6",
            },
            Id = "id6",
            Phase = Phase1.Active,
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
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



