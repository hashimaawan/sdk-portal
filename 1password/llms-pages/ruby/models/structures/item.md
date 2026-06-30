# Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkl0ZW0

*This model accepts additional fields of type Object.*


# Class Name

`Item`


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
item = Item.new(
  category: Category::SSH_KEY,
  vault: Vault1.new(
    id: 'id6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  favorite: false,
  id: 'id2',
  last_edited_by: 'lastEditedBy8',
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



