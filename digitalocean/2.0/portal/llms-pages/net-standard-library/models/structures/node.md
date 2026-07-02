# Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5vZGU

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Node`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was created. |
| `DropletId` | `string` | Optional | The ID of the Droplet used for the worker node. |
| `Id` | `Guid?` | Optional | A unique ID that can be used to identify and reference the node. |
| `Name` | `string` | Optional | An automatically generated, human-readable name for the node. |
| `Status` | [`Status10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/status-10.md) | Optional | An object containing a `state` attribute whose value is set to a string indicating the current status of the node. |
| `UpdatedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was last updated. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

Node node = new Node
{
    CreatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    DropletId = "205545370",
    Id = new Guid("e78247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f"),
    Name = "adoring-newton-3niq",
    Status = new Status10
    {
        State = State1.Provisioning,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    UpdatedAt = DateTime.ParseExact("2018-11-15T16:00:11Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



