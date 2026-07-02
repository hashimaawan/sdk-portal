# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Progress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ErrorSteps` | `int?` | Optional | - |
| `PendingSteps` | `int?` | Optional | - |
| `RunningSteps` | `int?` | Optional | - |
| `Steps` | [`List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `SuccessSteps` | `int?` | Optional | - |
| `SummarySteps` | [`List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `TotalSteps` | `int?` | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Progress progress = new Progress
{
    ErrorSteps = 3,
    PendingSteps = 2,
    RunningSteps = 2,
    Steps = new List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle>
    {
        new AStepThatIsRunAsPartOfTheDeploymentSLifecycle
        {
            ComponentName = "component_name0",
            EndedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            MessageBase = "message_base4",
            Name = "name2",
            Reason = new Reason
            {
                Code = "code2",
                Message = "message4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new AStepThatIsRunAsPartOfTheDeploymentSLifecycle
        {
            ComponentName = "component_name0",
            EndedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            MessageBase = "message_base4",
            Name = "name2",
            Reason = new Reason
            {
                Code = "code2",
                Message = "message4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new AStepThatIsRunAsPartOfTheDeploymentSLifecycle
        {
            ComponentName = "component_name0",
            EndedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            MessageBase = "message_base4",
            Name = "name2",
            Reason = new Reason
            {
                Code = "code2",
                Message = "message4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    SuccessSteps = 4,
    TotalSteps = 5,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



