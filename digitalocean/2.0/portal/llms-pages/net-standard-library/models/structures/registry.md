# Registry

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlZ2lzdHJ5

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Registry`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the registry was created. |
| `Name` | `string` | Optional | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` |
| `Region` | `string` | Optional | Slug of the region where registry data is stored |
| `StorageUsageBytes` | `int?` | Optional, Read-only | The amount of storage used in the registry in bytes. |
| `StorageUsageBytesUpdatedAt` | `DateTime?` | Optional, Read-only | The time at which the storage usage was updated. Storage usage is calculated asynchronously, and may not immediately reflect pushes to the registry. |
| `Subscription` | [`Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/subscription.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

Registry registry = new Registry
{
    CreatedAt = DateTime.ParseExact("2020-03-21T16:02:37Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Name = "example",
    Region = "fra1",
    StorageUsageBytes = 29393920,
    StorageUsageBytesUpdatedAt = DateTime.ParseExact("2020-11-04T21:39:49.530562231Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



