# Full Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkZ1bGxJdGVt

*This model accepts additional fields of type Object.*


# Class Name

`FullItem`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | [`Category`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/category.md) | Required | - |
| `created_at` | `DateTime` | Optional, Read-only | - |
| `favorite` | `TrueClass \| FalseClass` | Optional | **Default**: `false` |
| `id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `last_edited_by` | `String` | Optional, Read-only | - |
| `state` | [`State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/state.md) | Optional, Read-only | - |
| `tags` | `Array[String]` | Optional | - |
| `title` | `String` | Optional | - |
| `updated_at` | `DateTime` | Optional, Read-only | - |
| `urls` | [`Array[Url]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/url.md) | Optional | - |
| `vault` | [`Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/vault-1.md) | Required | - |
| `version` | `Integer` | Optional | - |
| `fields` | [`Array[Field]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/field.md) | Optional | - |
| `files` | [`Array[File]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/file.md) | Optional | - |
| `sections` | [`Array[Section2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/section-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
full_item = FullItem.new(
  category: Category::SOCIAL_SECURITY_NUMBER,
  vault: Vault1.new(
    id: 'id6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  favorite: false,
  id: 'id4',
  last_edited_by: 'lastEditedBy0',
  state: State::ARCHIVED,
  urls: [
    Url.new(
      href: 'https://example.com',
      primary: true
    ),
    Url.new(
      href: 'https://example.org'
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



