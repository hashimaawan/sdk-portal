# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type object.*


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/configuration.md) | Optional | - |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/tag.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

CreateWorkGroupInput createWorkGroupInput = new CreateWorkGroupInput
{
    Name = "Name6",
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
    Description = "Description0",
    Tags = new List<Tag>
    {
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



