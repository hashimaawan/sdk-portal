# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Pages1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `First` | `string` | Optional | URI of the first page of the results. |
| `Prev` | `string` | Optional | URI of the previous page of the results. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Pages1 pages1 = new Pages1
{
    First = "https://api.digitalocean.com/v2/images?page=1",
    Prev = "https://api.digitalocean.com/v2/images?page=1",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



