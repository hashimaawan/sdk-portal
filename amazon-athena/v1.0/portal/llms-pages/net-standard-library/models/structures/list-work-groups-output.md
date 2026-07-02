# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroups` | [`List<WorkGroupSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

ListWorkGroupsOutput listWorkGroupsOutput = new ListWorkGroupsOutput
{
    WorkGroups = new List<WorkGroupSummary>
    {
        new WorkGroupSummary
        {
            Name = "Name4",
            State = WorkGroupState1Enum.ENABLED,
            Description = "Description0",
            CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            EngineVersion = new EngineVersion1
            {
                SelectedEngineVersion = "SelectedEngineVersion4",
                EffectiveEngineVersion = "EffectiveEngineVersion6",
            },
        },
        new WorkGroupSummary
        {
            Name = "Name4",
            State = WorkGroupState1Enum.ENABLED,
            Description = "Description0",
            CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            EngineVersion = new EngineVersion1
            {
                SelectedEngineVersion = "SelectedEngineVersion4",
                EffectiveEngineVersion = "EffectiveEngineVersion6",
            },
        },
        new WorkGroupSummary
        {
            Name = "Name4",
            State = WorkGroupState1Enum.ENABLED,
            Description = "Description0",
            CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            EngineVersion = new EngineVersion1
            {
                SelectedEngineVersion = "SelectedEngineVersion4",
                EffectiveEngineVersion = "EffectiveEngineVersion6",
            },
        },
    },
    NextToken = "NextToken2",
};
```



