# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `txt_name` | `String` | Optional, Read-only | - |
| `txt_value` | `String` | Optional, Read-only | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
list_of_txt_validation_record = ListOfTxtValidationRecord.new(
  txt_name: '_acme-challenge.app.example.com',
  txt_value: 'lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



