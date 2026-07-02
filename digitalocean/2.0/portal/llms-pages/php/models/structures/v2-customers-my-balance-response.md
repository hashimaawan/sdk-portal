# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountBalance` | `?string` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. | getAccountBalance(): ?string | setAccountBalance(?string accountBalance): void |
| `generatedAt` | `?DateTime` | Optional | The time at which balances were most recently generated. | getGeneratedAt(): ?\DateTime | setGeneratedAt(?\DateTime generatedAt): void |
| `monthToDateBalance` | `?string` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. | getMonthToDateBalance(): ?string | setMonthToDateBalance(?string monthToDateBalance): void |
| `monthToDateUsage` | `?string` | Optional | Amount used in the current billing period as of the `generated_at` time. | getMonthToDateUsage(): ?string | setMonthToDateUsage(?string monthToDateUsage): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2CustomersMyBalanceResponseBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$v2CustomersMyBalanceResponse = V2CustomersMyBalanceResponseBuilder::init()
    ->accountBalance('12.23')
    ->generatedAt(DateTimeHelper::fromRfc3339DateTime('2019-07-09T15:01:12Z'))
    ->monthToDateBalance('23.44')
    ->monthToDateUsage('11.21')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



