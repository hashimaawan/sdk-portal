# V2 Customers My Invoices Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InvoiceItems` | [`List<InvoiceItem>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/invoice-item.md) | Optional | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2CustomersMyInvoicesResponse1 v2CustomersMyInvoicesResponse1 = new V2CustomersMyInvoicesResponse1
{
    Meta = new Meta
    {
        Total = 6,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    InvoiceItems = new List<InvoiceItem>
    {
        new InvoiceItem
        {
            Amount = "12.34",
            Description = "a56e086a317d8410c8b4cfd1f4dc9f82",
            Duration = "744",
            DurationUnit = "Hours",
            EndTime = "2020-02-01T00:00:00Z",
            GroupDescription = "my-doks-cluster",
            Product = "Kubernetes Clusters",
            ResourceUuid = "711157cb-37c8-4817-b371-44fa3504a39c",
            StartTime = "2020-01-01T00:00:00Z",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new InvoiceItem
        {
            Amount = "34.45",
            Description = "Spaces ($5/mo 250GB storage & 1TB bandwidth)",
            Duration = "744",
            DurationUnit = "Hours",
            EndTime = "2020-02-01T00:00:00Z",
            Product = "Spaces Subscription",
            StartTime = "2020-01-01T00:00:00Z",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=3&per_page=2",
                Next = "https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=2&per_page=2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



