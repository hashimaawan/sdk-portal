# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BlobsDeleted` | `int?` | Optional | The number of blobs deleted as a result of this garbage collection. |
| `CreatedAt` | `DateTime?` | Optional | The time the garbage collection was created. |
| `FreedBytes` | `int?` | Optional | The number of bytes freed as a result of this garbage collection. |
| `RegistryName` | `string` | Optional | The name of the container registry. |
| `Status` | [`Status15?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. |
| `UpdatedAt` | `DateTime?` | Optional | The time the garbage collection was last updated. |
| `Uuid` | `string` | Optional | A string specifying the UUID of the garbage collection. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

GarbageCollection garbageCollection = new GarbageCollection
{
    BlobsDeleted = 42,
    CreatedAt = DateTime.ParseExact("2020-10-30T21:03:24Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    FreedBytes = 667,
    RegistryName = "example",
    Status = Status15.Requested,
    UpdatedAt = DateTime.ParseExact("2020-10-30T21:03:44Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Uuid = "eff0feee-49c7-4e8f-ba5c-a320c109c8a8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



