# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | [`WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/work-group-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Globalization;

GetWorkGroupOutput getWorkGroupOutput = new GetWorkGroupOutput
{
    WorkGroup = new WorkGroup2
    {
        Name = "Name2",
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
        Description = "Description4",
        CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
    },
};
```



