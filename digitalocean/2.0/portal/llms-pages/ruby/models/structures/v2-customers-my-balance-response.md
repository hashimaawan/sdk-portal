# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_balance` | `String` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. |
| `generated_at` | `DateTime` | Optional | The time at which balances were most recently generated. |
| `month_to_date_balance` | `String` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. |
| `month_to_date_usage` | `String` | Optional | Amount used in the current billing period as of the `generated_at` time. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_customers_my_balance_response = V2CustomersMyBalanceResponse.new(
  account_balance: '12.23',
  generated_at: DateTimeHelper.from_rfc3339('2019-07-09T15:01:12Z'),
  month_to_date_balance: '23.44',
  month_to_date_usage: '11.21',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



