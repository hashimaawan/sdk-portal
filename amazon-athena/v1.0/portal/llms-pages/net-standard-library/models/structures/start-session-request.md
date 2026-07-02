# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineConfiguration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-configuration-1.md) | Required | - |
| `NotebookVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SessionIdleTimeoutInMinutes` | `int?` | Optional | **Constraints**: `>= 1`, `<= 480` |
| `ClientRequestToken` | `string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

StartSessionRequest startSessionRequest = new StartSessionRequest
{
    WorkGroup = "WorkGroup2",
    EngineConfiguration = new EngineConfiguration1
    {
        MaxConcurrentDpus = 94,
        CoordinatorDpuSize = 1,
        DefaultExecutorDpuSize = 1,
        AdditionalConfigs = new AdditionalConfigs
        {
            ["exampleAdditionalProperty"] = "AdditionalConfigs_additionalProperties5",
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Description = "Description4",
    NotebookVersion = "NotebookVersion4",
    SessionIdleTimeoutInMinutes = 172,
    ClientRequestToken = "ClientRequestToken4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



