# V2 Customers My Billing History Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCaWxsaW5nJTI1MjBIaXN0b3J5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2CustomersMyBillingHistoryResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BillingHistory` | [`List<BillingHistory>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/billing-history.md) | Optional | - | List<BillingHistory> getBillingHistory() | setBillingHistory(List<BillingHistory> billingHistory) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta-1.md) | Required | Information about the response itself. | Meta1 getMeta() | setMeta(Meta1 meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.BillingHistory;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta1;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.Type6;
import com.digitalocean.api.models.V2CustomersMyBillingHistoryResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2CustomersMyBillingHistoryResponse v2CustomersMyBillingHistoryResponse = new V2CustomersMyBillingHistoryResponse.Builder(
    new Meta1.Builder()
        .total(5)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.billingHistory(Arrays.asList(
        new BillingHistory.Builder()
            .amount("12.34")
            .date(DateTimeHelper.fromRfc8601DateTime("2018-06-01T08:44:38Z"))
            .description("Invoice for May 2018")
            .invoiceId("123")
            .invoiceUuid("example-uuid")
            .type(Type6.INVOICE)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new BillingHistory.Builder()
            .amount("-12.34")
            .date(DateTimeHelper.fromRfc8601DateTime("2018-06-02T08:44:38Z"))
            .description("Payment (MC 2018)")
            .invoiceId("invoice_id6")
            .invoiceUuid("invoice_uuid4")
            .type(Type6.PAYMENT)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/customers/my/billing_history?page=3&per_page=2")
                .next("https://api.digitalocean.com/v2/customers/my/billing_history?page=2&per_page=2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



