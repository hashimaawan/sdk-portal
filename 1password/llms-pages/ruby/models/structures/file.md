# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type Object.*


# Class Name

`File`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `String` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. |
| `content_path` | `String` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. |
| `id` | `String` | Optional | ID of the file |
| `name` | `String` | Optional | Name of the file |
| `section` | [`Section1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. |
| `size` | `Integer` | Optional | Size in bytes of the file |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
file = File.new(
  content: 'VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo=',
  content_path: 'v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content',
  id: '6r65pjq33banznomn7q22sj44e',
  name: 'foo.txt',
  section: Section1.new(
    id: 'id6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  size: 35,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



