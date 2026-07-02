# Backup Restore

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhY2t1cFJlc3RvcmU

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`BackupRestore`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BackupCreatedAt` | `DateTime?` | Optional | The timestamp of an existing database cluster backup in ISO8601 combined date and time format. The most recent backup will be used if excluded. |
| `DatabaseName` | `string` | Required | The name of an existing database cluster from which the backup will be restored. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

BackupRestore backupRestore = new BackupRestore
{
    DatabaseName = "backend",
    BackupCreatedAt = DateTime.ParseExact("2019-01-31T19:25:22Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



