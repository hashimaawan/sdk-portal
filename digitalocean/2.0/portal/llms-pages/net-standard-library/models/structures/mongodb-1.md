# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EndOfAvailability` | `string` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `EndOfLife` | `string` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `Version` | `string` | Optional | The engine version. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Mongodb1 mongodb1 = new Mongodb1
{
    EndOfAvailability = "2023-05-09T00:00:00Z",
    EndOfLife = "2023-11-09T00:00:00Z",
    Version = "8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



