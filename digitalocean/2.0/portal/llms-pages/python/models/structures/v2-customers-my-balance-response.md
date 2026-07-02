# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_balance` | `str` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. |
| `generated_at` | `datetime` | Optional | The time at which balances were most recently generated. |
| `month_to_date_balance` | `str` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. |
| `month_to_date_usage` | `str` | Optional | Amount used in the current billing period as of the `generated_at` time. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.v_2_customers_my_balance_response import V2CustomersMyBalanceResponse

v_2_customers_my_balance_response = V2CustomersMyBalanceResponse(
    account_balance='12.23',
    generated_at=dateutil.parser.parse('2019-07-09T15:01:12Z'),
    month_to_date_balance='23.44',
    month_to_date_usage='11.21',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



