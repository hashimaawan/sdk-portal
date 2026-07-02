# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AccountBalance` | `string` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. |
| `GeneratedAt` | `DateTime?` | Optional | The time at which balances were most recently generated. |
| `MonthToDateBalance` | `string` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. |
| `MonthToDateUsage` | `string` | Optional | Amount used in the current billing period as of the `generated_at` time. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

V2CustomersMyBalanceResponse v2CustomersMyBalanceResponse = new V2CustomersMyBalanceResponse
{
    AccountBalance = "12.23",
    GeneratedAt = DateTime.ParseExact("2019-07-09T15:01:12Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    MonthToDateBalance = "23.44",
    MonthToDateUsage = "11.21",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



