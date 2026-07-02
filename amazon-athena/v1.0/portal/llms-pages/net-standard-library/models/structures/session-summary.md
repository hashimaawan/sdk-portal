# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.

*This model accepts additional fields of type object.*


# Class Name

`SessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-version-1.md) | Optional | - |
| `NotebookVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/status-3.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

SessionSummary sessionSummary = new SessionSummary
{
    SessionId = "SessionId0",
    Description = "Description8",
    EngineVersion = new EngineVersion1
    {
        SelectedEngineVersion = "SelectedEngineVersion4",
        EffectiveEngineVersion = "EffectiveEngineVersion6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    NotebookVersion = "NotebookVersion2",
    Status = new Status3
    {
        StartDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        LastModifiedDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        EndDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        IdleSinceDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        State = SessionState1.Terminating,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



