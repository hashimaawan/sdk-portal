# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountBalance` | `String` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. | String getAccountBalance() | setAccountBalance(String accountBalance) |
| `GeneratedAt` | `LocalDateTime` | Optional | The time at which balances were most recently generated. | LocalDateTime getGeneratedAt() | setGeneratedAt(LocalDateTime generatedAt) |
| `MonthToDateBalance` | `String` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. | String getMonthToDateBalance() | setMonthToDateBalance(String monthToDateBalance) |
| `MonthToDateUsage` | `String` | Optional | Amount used in the current billing period as of the `generated_at` time. | String getMonthToDateUsage() | setMonthToDateUsage(String monthToDateUsage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.V2CustomersMyBalanceResponse;
import java.io.IOException;

V2CustomersMyBalanceResponse v2CustomersMyBalanceResponse = new V2CustomersMyBalanceResponse.Builder()
    .accountBalance("12.23")
    .generatedAt(DateTimeHelper.fromRfc8601DateTime("2019-07-09T15:01:12Z"))
    .monthToDateBalance("23.44")
    .monthToDateUsage("11.21")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



