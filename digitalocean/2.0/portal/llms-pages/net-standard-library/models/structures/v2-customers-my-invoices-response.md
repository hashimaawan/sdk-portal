# V2 Customers My Invoices Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InvoicePreview` | [`InvoicePreview`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/invoice-preview.md) | Optional | The invoice preview. |
| `Invoices` | [`List<InvoicePreview>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/invoice-preview.md) | Optional | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2CustomersMyInvoicesResponse v2CustomersMyInvoicesResponse = new V2CustomersMyInvoicesResponse
{
    Meta = new Meta
    {
        Total = 70,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    InvoicePreview = new InvoicePreview
    {
        Amount = "34.56",
        InvoicePeriod = "2020-02",
        InvoiceUuid = "1afe95e6-0958-4eb0-8d9a-9c5060d3ef03",
        UpdatedAt = "2020-02-23T06:31:50Z",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Invoices = new List<InvoicePreview>
    {
        new InvoicePreview
        {
            Amount = "12.34",
            InvoicePeriod = "2019-12",
            InvoiceUuid = "22737513-0ea7-4206-8ceb-98a575af7681",
            UpdatedAt = "updated_at8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new InvoicePreview
        {
            Amount = "23.45",
            InvoicePeriod = "2019-11",
            InvoiceUuid = "fdabb512-6faf-443c-ba2e-665452332a9e",
            UpdatedAt = "updated_at8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "https://api.digitalocean.com/v2/customers/my/invoices?page=35&per_page=2",
                Next = "https://api.digitalocean.com/v2/customers/my/invoices?page=2&per_page=2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



