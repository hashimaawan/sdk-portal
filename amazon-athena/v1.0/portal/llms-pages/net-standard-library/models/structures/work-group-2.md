# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRldvcmtHcm91cDI

*This model accepts additional fields of type object.*


# Class Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `State` | [`WorkGroupState3?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/work-group-state-3.md) | Optional | - |
| `Configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/configuration.md) | Optional | - |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `CreationTime` | `DateTime?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

WorkGroup2 workGroup2 = new WorkGroup2
{
    Name = "Name0",
    State = WorkGroupState3.Enabled,
    Configuration = new Configuration
    {
        ResultConfiguration = new ResultConfiguration1
        {
            OutputLocation = "OutputLocation0",
            EncryptionConfiguration = new EncryptionConfiguration2
            {
                EncryptionOption = EncryptionOption1.SseS3,
                KmsKey = "KmsKey6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ExpectedBucketOwner = "ExpectedBucketOwner0",
            AclConfiguration = new AclConfiguration1
            {
                S3AclOption = S3AclOption1.BucketOwnerFullControl,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        EnforceWorkGroupConfiguration = false,
        PublishCloudWatchMetricsEnabled = false,
        BytesScannedCutoffPerQuery = 10000000,
        RequesterPaysEnabled = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Description = "Description6",
    CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



