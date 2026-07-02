# V2 Customers My Invoices Summary Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwU3VtbWFyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesSummaryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `String` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `billing_period` | `String` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `credits_and_adjustments` | [`CreditsAndAdjustments`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/credits-and-adjustments.md) | Optional | - |
| `invoice_uuid` | `String` | Optional | UUID of the invoice |
| `overages` | [`Overages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/overages.md) | Optional | - |
| `product_charges` | [`ProductCharges`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/product-charges.md) | Optional | - |
| `taxes` | [`Taxes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/taxes.md) | Optional | - |
| `user_billing_address` | [`UserBillingAddress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/user-billing-address.md) | Optional | - |
| `user_company` | `String` | Optional | Company of the DigitalOcean customer being invoiced, if set. |
| `user_email` | `String` | Optional | Email of the DigitalOcean customer being invoiced. |
| `user_name` | `String` | Optional | Name of the DigitalOcean customer being invoiced. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_customers_my_invoices_summary_response = V2CustomersMyInvoicesSummaryResponse.new(
  amount: '27.13',
  billing_period: '2020-01',
  credits_and_adjustments: CreditsAndAdjustments.new(
    amount: 'amount6',
    name: 'name4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  invoice_uuid: '22737513-0ea7-4206-8ceb-98a575af7681',
  overages: Overages.new(
    amount: 'amount6',
    name: 'name4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  user_company: 'DigitalOcean',
  user_email: 'sammy@digitalocean.com',
  user_name: 'Sammy Shark',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



