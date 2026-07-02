# Batch Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeUlucHV0

Contains an array of named query IDs.

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_ids` | `Array[String]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
batch_get_named_query_input = BatchGetNamedQueryInput.new(
  named_query_ids: [
    'NamedQueryIds3',
    'NamedQueryIds2',
    'NamedQueryIds1'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



