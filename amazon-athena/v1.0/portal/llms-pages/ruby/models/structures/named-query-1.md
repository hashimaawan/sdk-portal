# Named Query 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk5hbWVkUXVlcnkx

*This model accepts additional fields of type Object.*


# Class Name

`NamedQuery1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `database` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `query_string` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `named_query_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
named_query1 = NamedQuery1.new(
  name: 'Name0',
  database: 'Database8',
  query_string: 'QueryString2',
  description: 'Description4',
  named_query_id: 'NamedQueryId2',
  work_group: 'WorkGroup2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



