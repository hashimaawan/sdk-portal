# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `ConfigurationUpdates` | [`ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/configuration-updates.md) | Optional | - |
| `State` | [`WorkGroupState2Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/work-group-state-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

UpdateWorkGroupInput updateWorkGroupInput = new UpdateWorkGroupInput
{
    WorkGroup = "WorkGroup0",
    Description = "Description8",
    ConfigurationUpdates = new ConfigurationUpdates
    {
        EnforceWorkGroupConfiguration = false,
        ResultConfigurationUpdates = new ResultConfigurationUpdates2
        {
            OutputLocation = "OutputLocation0",
            RemoveOutputLocation = false,
            EncryptionConfiguration = new EncryptionConfiguration2
            {
                EncryptionOption = EncryptionOption1Enum.SSES3,
                KmsKey = "KmsKey6",
            },
            RemoveEncryptionConfiguration = false,
            ExpectedBucketOwner = "ExpectedBucketOwner0",
        },
        PublishCloudWatchMetricsEnabled = false,
        BytesScannedCutoffPerQuery = 10000000,
        RemoveBytesScannedCutoffPerQuery = false,
    },
    State = WorkGroupState2Enum.ENABLED,
};
```



