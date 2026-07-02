# V2 Databases Config Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesConfigResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Config` | [`V2DatabasesConfigResponseConfig`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/v2-databases-config-response-config.md) | Required | This is a container for any-of cases. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;

V2DatabasesConfigResponse v2DatabasesConfigResponse = new V2DatabasesConfigResponse
{
    Config = V2DatabasesConfigResponseConfig.FromConfig(
        new Config
        {
            BackupHour = 3,
            BackupMinute = 30,
            BinlogRetentionPeriod = 600,
            ConnectTimeout = 10,
            DefaultTimeZone = "+03:00",
            GroupConcatMaxLen = 1024,
            InformationSchemaStatsExpiry = 86400,
            InnodbFtMinTokenSize = 3,
            InnodbFtServerStopwordTable = "db_name/table_name",
            InnodbLockWaitTimeout = 50,
            InnodbLogBufferSize = 16777216,
            InnodbOnlineAlterLogMaxSize = 134217728,
            InnodbPrintAllDeadlocks = true,
            InnodbRollbackOnTimeout = true,
            InteractiveTimeout = 3600,
            InternalTmpMemStorageEngine = InternalTmpMemStorageEngine.TempTable,
            LongQueryTime = 10,
            MaxAllowedPacket = 67108864,
            MaxHeapTableSize = 16777216,
            NetReadTimeout = 30,
            NetWriteTimeout = 30,
            SlowQueryLog = true,
            SortBufferSize = 262144,
            SqlMode = "ANSI,TRADITIONAL",
            SqlRequirePrimaryKey = true,
            TmpTableSize = 16777216,
            WaitTimeout = 28800,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        }
    ),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



