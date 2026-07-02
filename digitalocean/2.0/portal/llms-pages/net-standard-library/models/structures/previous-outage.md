# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DurationSeconds` | `int?` | Optional | - |
| `EndedAt` | `string` | Optional | - |
| `Region` | `string` | Optional | - |
| `StartedAt` | `string` | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

PreviousOutage previousOutage = new PreviousOutage
{
    DurationSeconds = 120,
    EndedAt = "2022-03-17T18:06:55Z",
    Region = "us_east",
    StartedAt = "2022-03-17T18:04:55Z",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



