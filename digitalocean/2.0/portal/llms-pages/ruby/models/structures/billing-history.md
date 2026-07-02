# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `String` | Optional | Amount of the billing history entry. |
| `date` | `DateTime` | Optional | Time the billing history entry occurred. |
| `description` | `String` | Optional | Description of the billing history entry. |
| `invoice_id` | `String` | Optional | ID of the invoice associated with the billing history entry, if  applicable. |
| `invoice_uuid` | `String` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. |
| `type` | [`Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-6.md) | Optional | Type of billing history entry. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
billing_history = BillingHistory.new(
  amount: '12.34',
  date: DateTimeHelper.from_rfc3339('2018-06-01T08:44:38Z'),
  description: 'Invoice for May 2018',
  invoice_id: '123',
  invoice_uuid: 'example-uuid',
  type: Type6::INVOICE,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



