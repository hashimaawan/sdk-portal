# Invoice Preview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkludm9pY2VQcmV2aWV3

The invoice preview.

*This model accepts additional fields of type Object.*


# Class Name

`InvoicePreview`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. | String getAmount() | setAmount(String amount) |
| `InvoicePeriod` | `String` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. | String getInvoicePeriod() | setInvoicePeriod(String invoicePeriod) |
| `InvoiceUuid` | `String` | Optional | The UUID of the invoice. The canonical reference for the invoice. | String getInvoiceUuid() | setInvoiceUuid(String invoiceUuid) |
| `UpdatedAt` | `String` | Optional | Time the invoice was last updated.  This is only included with the invoice preview. | String getUpdatedAt() | setUpdatedAt(String updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InvoicePreview;
import java.io.IOException;

InvoicePreview invoicePreview = new InvoicePreview.Builder()
    .amount("23.45")
    .invoicePeriod("2020-01")
    .invoiceUuid("fdabb512-6faf-443c-ba2e-665452332a9e")
    .updatedAt("2020-01-23T06:31:50Z")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



