# Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRldvcmtHcm91cA

A workgroup, which contains a name, description, creation time, state, and other configuration, listed under <a>WorkGroup$Configuration</a>. Each workgroup enables you to isolate queries for you or your group of users from other queries in the same account, to configure the query results location and the encryption configuration (known as workgroup settings), to enable sending query metrics to Amazon CloudWatch, and to establish per-query data usage control limits for all queries in a workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type object.*


# Class Name

`WorkGroup`


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

WorkGroup workGroup = new WorkGroup
{
    Name = "Name2",
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



