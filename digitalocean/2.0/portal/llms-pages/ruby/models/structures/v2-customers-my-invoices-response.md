# V2 Customers My Invoices Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoice_preview` | [`InvoicePreview`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/invoice-preview.md) | Optional | The invoice preview. |
| `invoices` | [`Array[InvoicePreview]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/invoice-preview.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_customers_my_invoices_response = V2CustomersMyInvoicesResponse.new(
  meta: Meta.new(
    total: 70,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  invoice_preview: InvoicePreview.new(
    amount: '34.56',
    invoice_period: '2020-02',
    invoice_uuid: '1afe95e6-0958-4eb0-8d9a-9c5060d3ef03',
    updated_at: '2020-02-23T06:31:50Z',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  invoices: [
    InvoicePreview.new(
      amount: '12.34',
      invoice_period: '2019-12',
      invoice_uuid: '22737513-0ea7-4206-8ceb-98a575af7681',
      updated_at: 'updated_at8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    InvoicePreview.new(
      amount: '23.45',
      invoice_period: '2019-11',
      invoice_uuid: 'fdabb512-6faf-443c-ba2e-665452332a9e',
      updated_at: 'updated_at8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'https://api.digitalocean.com/v2/customers/my/invoices?page=35&per_page=2',
      mnext: 'https://api.digitalocean.com/v2/customers/my/invoices?page=2&per_page=2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



