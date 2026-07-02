# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Pages`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Last` | `string` | Optional | URI of the last page of the results. |
| `Next` | `string` | Optional | URI of the next page of the results. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Pages pages = new Pages
{
    Last = "https://api.digitalocean.com/v2/images?page=2",
    Next = "https://api.digitalocean.com/v2/images?page=2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



