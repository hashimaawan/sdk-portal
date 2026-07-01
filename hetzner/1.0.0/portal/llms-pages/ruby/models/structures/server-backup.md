# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type Object.*


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `String` | Required | Percentage by how much the base price will increase |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server_backup = ServerBackup.new(
  percentage: '20.0000000000',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



