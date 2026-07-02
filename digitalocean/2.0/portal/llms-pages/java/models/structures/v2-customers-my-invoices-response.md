# V2 Customers My Invoices Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2CustomersMyInvoicesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `InvoicePreview` | [`InvoicePreview`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/invoice-preview.md) | Optional | The invoice preview. | InvoicePreview getInvoicePreview() | setInvoicePreview(InvoicePreview invoicePreview) |
| `Invoices` | [`List<InvoicePreview>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/invoice-preview.md) | Optional | - | List<InvoicePreview> getInvoices() | setInvoices(List<InvoicePreview> invoices) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InvoicePreview;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.V2CustomersMyInvoicesResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2CustomersMyInvoicesResponse v2CustomersMyInvoicesResponse = new V2CustomersMyInvoicesResponse.Builder(
    new Meta.Builder(
        70
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.invoicePreview(new InvoicePreview.Builder()
        .amount("34.56")
        .invoicePeriod("2020-02")
        .invoiceUuid("1afe95e6-0958-4eb0-8d9a-9c5060d3ef03")
        .updatedAt("2020-02-23T06:31:50Z")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.invoices(Arrays.asList(
        new InvoicePreview.Builder()
            .amount("12.34")
            .invoicePeriod("2019-12")
            .invoiceUuid("22737513-0ea7-4206-8ceb-98a575af7681")
            .updatedAt("updated_at8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new InvoicePreview.Builder()
            .amount("23.45")
            .invoicePeriod("2019-11")
            .invoiceUuid("fdabb512-6faf-443c-ba2e-665452332a9e")
            .updatedAt("updated_at8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/customers/my/invoices?page=35&per_page=2")
                .next("https://api.digitalocean.com/v2/customers/my/invoices?page=2&per_page=2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



