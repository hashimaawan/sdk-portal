# Invoice Preview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkludm9pY2VQcmV2aWV3

The invoice preview.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`InvoicePreview`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `String` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `invoice_period` | `String` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `invoice_uuid` | `String` | Optional | The UUID of the invoice. The canonical reference for the invoice. |
| `updated_at` | `String` | Optional | Time the invoice was last updated.  This is only included with the invoice preview. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
invoice_preview = InvoicePreview.new(
  amount: '23.45',
  invoice_period: '2020-01',
  invoice_uuid: 'fdabb512-6faf-443c-ba2e-665452332a9e',
  updated_at: '2020-01-23T06:31:50Z',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



