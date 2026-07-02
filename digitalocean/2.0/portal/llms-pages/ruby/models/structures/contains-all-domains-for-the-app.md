# Contains All Domains for the App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbnRhaW5zJTI1MjBhbGwlMjUyMGRvbWFpbnMlMjUyMGZvciUyNTIwdGhlJTI1MjBhcHA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ContainsAllDomainsForTheApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_expires_at` | `DateTime` | Optional, Read-only | - |
| `id` | `String` | Optional | - |
| `phase` | [`Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1::UNKNOWN` |
| `progress` | [`Progress1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/progress-1.md) | Optional | - |
| `rotate_validation_records` | `TrueClass \| FalseClass` | Optional, Read-only | - |
| `spec` | [`Domain`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/domain.md) | Optional | - |
| `validations` | [`Array[ListOfTxtValidationRecord]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/list-of-txt-validation-record.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
contains_all_domains_for_the_app = ContainsAllDomainsForTheApp.new(
  certificate_expires_at: DateTimeHelper.from_rfc3339('2024-01-29T23:59:59Z'),
  id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  phase: Phase1::ACTIVE,
  progress: Progress1.new(
    steps: [
      { 'key1' => 'val1', 'key2' => 'val2' },
      { 'key1' => 'val1', 'key2' => 'val2' },
      { 'key1' => 'val1', 'key2' => 'val2' }
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  rotate_validation_records: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



