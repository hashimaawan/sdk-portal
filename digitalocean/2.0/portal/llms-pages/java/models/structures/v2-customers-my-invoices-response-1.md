# V2 Customers My Invoices Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`V2CustomersMyInvoicesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `InvoiceItems` | [`List<InvoiceItem>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/invoice-item.md) | Optional | - | List<InvoiceItem> getInvoiceItems() | setInvoiceItems(List<InvoiceItem> invoiceItems) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InvoiceItem;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.V2CustomersMyInvoicesResponse1;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2CustomersMyInvoicesResponse1 v2CustomersMyInvoicesResponse1 = new V2CustomersMyInvoicesResponse1.Builder(
    new Meta.Builder(
        6
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.invoiceItems(Arrays.asList(
        new InvoiceItem.Builder()
            .amount("12.34")
            .description("a56e086a317d8410c8b4cfd1f4dc9f82")
            .duration("744")
            .durationUnit("Hours")
            .endTime("2020-02-01T00:00:00Z")
            .groupDescription("my-doks-cluster")
            .product("Kubernetes Clusters")
            .resourceUuid("711157cb-37c8-4817-b371-44fa3504a39c")
            .startTime("2020-01-01T00:00:00Z")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new InvoiceItem.Builder()
            .amount("34.45")
            .description("Spaces ($5/mo 250GB storage & 1TB bandwidth)")
            .duration("744")
            .durationUnit("Hours")
            .endTime("2020-02-01T00:00:00Z")
            .product("Spaces Subscription")
            .startTime("2020-01-01T00:00:00Z")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=3&per_page=2")
                .next("https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=2&per_page=2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



