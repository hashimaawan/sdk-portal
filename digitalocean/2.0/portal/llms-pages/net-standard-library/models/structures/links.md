# Links

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpbmtz

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Links`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pages` | [`LinksPages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/links-pages.md) | Optional | This is a container for any-of cases. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;

Links links = new Links
{
    Pages = LinksPages.FromPages(
        new Pages
        {
            Last = "last6",
            Next = "next2",
            ["pages"] = ApiHelper.JsonDeserialize<object>("{\"first\":\"https://api.digitalocean.com/v2/account/keys?page=1\",\"prev\":\"https://api.digitalocean.com/v2/account/keys?page=2\"}"),
        }
    ),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



