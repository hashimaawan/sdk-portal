# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_named_query_output = CreateNamedQueryOutput.new(
  named_query_id: 'NamedQueryId4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



