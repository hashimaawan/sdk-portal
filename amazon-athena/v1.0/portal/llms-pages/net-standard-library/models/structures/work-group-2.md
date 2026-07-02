# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRldvcmtHcm91cDI


# Class Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `State` | [`WorkGroupState3Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/work-group-state-3.md) | Optional | - |
| `Configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/configuration.md) | Optional | - |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `CreationTime` | `DateTime?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Globalization;

WorkGroup2 workGroup2 = new WorkGroup2
{
    Name = "Name0",
    State = WorkGroupState3Enum.ENABLED,
    Configuration = new Configuration
    {
        ResultConfiguration = new ResultConfiguration1
        {
            OutputLocation = "OutputLocation0",
            EncryptionConfiguration = new EncryptionConfiguration2
            {
                EncryptionOption = EncryptionOption1Enum.SSES3,
                KmsKey = "KmsKey6",
            },
            ExpectedBucketOwner = "ExpectedBucketOwner0",
            AclConfiguration = new AclConfiguration1
            {
                S3AclOption = S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
            },
        },
        EnforceWorkGroupConfiguration = false,
        PublishCloudWatchMetricsEnabled = false,
        BytesScannedCutoffPerQuery = 10000000,
        RequesterPaysEnabled = false,
    },
    Description = "Description6",
    CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
};
```



