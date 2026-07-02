# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `Sessions` | [`List<SessionSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

ListSessionsResponse listSessionsResponse = new ListSessionsResponse
{
    NextToken = "NextToken6",
    Sessions = new List<SessionSummary>
    {
        new SessionSummary
        {
            SessionId = "SessionId6",
            Description = "Description4",
            EngineVersion = new EngineVersion1
            {
                SelectedEngineVersion = "SelectedEngineVersion4",
                EffectiveEngineVersion = "EffectiveEngineVersion6",
            },
            NotebookVersion = "NotebookVersion6",
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
                State = SessionState1Enum.TERMINATING,
            },
        },
        new SessionSummary
        {
            SessionId = "SessionId6",
            Description = "Description4",
            EngineVersion = new EngineVersion1
            {
                SelectedEngineVersion = "SelectedEngineVersion4",
                EffectiveEngineVersion = "EffectiveEngineVersion6",
            },
            NotebookVersion = "NotebookVersion6",
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
                State = SessionState1Enum.TERMINATING,
            },
        },
        new SessionSummary
        {
            SessionId = "SessionId6",
            Description = "Description4",
            EngineVersion = new EngineVersion1
            {
                SelectedEngineVersion = "SelectedEngineVersion4",
                EffectiveEngineVersion = "EffectiveEngineVersion6",
            },
            NotebookVersion = "NotebookVersion6",
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
                State = SessionState1Enum.TERMINATING,
            },
        },
    },
};
```



