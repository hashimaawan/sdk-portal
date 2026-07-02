# Timescaledb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlRpbWVzY2FsZWRi

TimescaleDB extension configuration values

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Timescaledb`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `max_background_workers` | `Integer` | Optional | The number of background workers for timescaledb operations.  Set to the sum of your number of databases and the total number of concurrent background workers you want running at any given point in time.<br><br>**Constraints**: `>= 1`, `<= 4096` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
timescaledb = Timescaledb.new(
  max_background_workers: 8,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



