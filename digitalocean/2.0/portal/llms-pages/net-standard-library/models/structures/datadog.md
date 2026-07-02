# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Datadog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApiKey` | `string` | Required | Datadog API key. |
| `Endpoint` | `string` | Optional | Datadog HTTP log intake endpoint. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Datadog datadog = new Datadog
{
    ApiKey = "abcdefghijklmnopqrstuvwxyz0123456789",
    Endpoint = "https://mydatadogendpoint.com",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



