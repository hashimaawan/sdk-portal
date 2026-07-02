# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountBalance` | `string \| undefined` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. |
| `generatedAt` | `string \| undefined` | Optional | The time at which balances were most recently generated. |
| `monthToDateBalance` | `string \| undefined` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. |
| `monthToDateUsage` | `string \| undefined` | Optional | Amount used in the current billing period as of the `generated_at` time. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CustomersMyBalanceResponse } from 'digitalocean-apilib';

const v2CustomersMyBalanceResponse: V2CustomersMyBalanceResponse = {
  accountBalance: '12.23',
  generatedAt: '2019-07-09T15:01:12Z',
  monthToDateBalance: '23.44',
  monthToDateUsage: '11.21',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



