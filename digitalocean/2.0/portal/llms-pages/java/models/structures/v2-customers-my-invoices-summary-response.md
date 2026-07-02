# V2 Customers My Invoices Summary Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwU3VtbWFyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2CustomersMyInvoicesSummaryResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. | String getAmount() | setAmount(String amount) |
| `BillingPeriod` | `String` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. | String getBillingPeriod() | setBillingPeriod(String billingPeriod) |
| `CreditsAndAdjustments` | [`CreditsAndAdjustments`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/credits-and-adjustments.md) | Optional | - | CreditsAndAdjustments getCreditsAndAdjustments() | setCreditsAndAdjustments(CreditsAndAdjustments creditsAndAdjustments) |
| `InvoiceUuid` | `String` | Optional | UUID of the invoice | String getInvoiceUuid() | setInvoiceUuid(String invoiceUuid) |
| `Overages` | [`Overages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/overages.md) | Optional | - | Overages getOverages() | setOverages(Overages overages) |
| `ProductCharges` | [`ProductCharges`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/product-charges.md) | Optional | - | ProductCharges getProductCharges() | setProductCharges(ProductCharges productCharges) |
| `Taxes` | [`Taxes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/taxes.md) | Optional | - | Taxes getTaxes() | setTaxes(Taxes taxes) |
| `UserBillingAddress` | [`UserBillingAddress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/user-billing-address.md) | Optional | - | UserBillingAddress getUserBillingAddress() | setUserBillingAddress(UserBillingAddress userBillingAddress) |
| `UserCompany` | `String` | Optional | Company of the DigitalOcean customer being invoiced, if set. | String getUserCompany() | setUserCompany(String userCompany) |
| `UserEmail` | `String` | Optional | Email of the DigitalOcean customer being invoiced. | String getUserEmail() | setUserEmail(String userEmail) |
| `UserName` | `String` | Optional | Name of the DigitalOcean customer being invoiced. | String getUserName() | setUserName(String userName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.CreditsAndAdjustments;
import com.digitalocean.api.models.Overages;
import com.digitalocean.api.models.V2CustomersMyInvoicesSummaryResponse;
import java.io.IOException;

V2CustomersMyInvoicesSummaryResponse v2CustomersMyInvoicesSummaryResponse = new V2CustomersMyInvoicesSummaryResponse.Builder()
    .amount("27.13")
    .billingPeriod("2020-01")
    .creditsAndAdjustments(new CreditsAndAdjustments.Builder()
        .amount("amount6")
        .name("name4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .invoiceUuid("22737513-0ea7-4206-8ceb-98a575af7681")
    .overages(new Overages.Builder()
        .amount("amount6")
        .name("name4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .userCompany("DigitalOcean")
    .userEmail("sammy@digitalocean.com")
    .userName("Sammy Shark")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



