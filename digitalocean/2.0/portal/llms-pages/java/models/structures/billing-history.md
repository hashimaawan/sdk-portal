# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type Object.*


# Class Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Amount of the billing history entry. | String getAmount() | setAmount(String amount) |
| `Date` | `LocalDateTime` | Optional | Time the billing history entry occurred. | LocalDateTime getDate() | setDate(LocalDateTime date) |
| `Description` | `String` | Optional | Description of the billing history entry. | String getDescription() | setDescription(String description) |
| `InvoiceId` | `String` | Optional | ID of the invoice associated with the billing history entry, if  applicable. | String getInvoiceId() | setInvoiceId(String invoiceId) |
| `InvoiceUuid` | `String` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. | String getInvoiceUuid() | setInvoiceUuid(String invoiceUuid) |
| `Type` | [`Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-6.md) | Optional | Type of billing history entry. | Type6 getType() | setType(Type6 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.BillingHistory;
import com.digitalocean.api.models.Type6;
import java.io.IOException;

BillingHistory billingHistory = new BillingHistory.Builder()
    .amount("12.34")
    .date(DateTimeHelper.fromRfc8601DateTime("2018-06-01T08:44:38Z"))
    .description("Invoice for May 2018")
    .invoiceId("123")
    .invoiceUuid("example-uuid")
    .type(Type6.INVOICE)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



