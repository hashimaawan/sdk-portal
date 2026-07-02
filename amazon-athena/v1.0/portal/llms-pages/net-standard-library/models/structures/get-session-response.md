# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ


# Class Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `WorkGroup` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `EngineConfiguration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-configuration-1.md) | Optional | - |
| `NotebookVersion` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SessionConfiguration` | [`SessionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/session-configuration-2.md) | Optional | - |
| `Status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/status-3.md) | Optional | - |
| `Statistics` | [`Statistics3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/statistics-3.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetSessionResponse getSessionResponse = new GetSessionResponse
{
    SessionId = "SessionId6",
    Description = "Description4",
    WorkGroup = "WorkGroup4",
    EngineVersion = "EngineVersion8",
    EngineConfiguration = new EngineConfiguration1
    {
        MaxConcurrentDpus = 94,
        CoordinatorDpuSize = 1,
        DefaultExecutorDpuSize = 1,
        AdditionalConfigs = new AdditionalConfigs
        {
        },
    },
};
```



