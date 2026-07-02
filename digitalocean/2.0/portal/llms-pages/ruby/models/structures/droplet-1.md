# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Droplet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destroyed_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. |
| `error_message` | `String` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. |
| `id` | `String` | Optional | The unique identifier for the resource scheduled for deletion. |
| `name` | `String` | Optional | The name of the resource scheduled for deletion. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
droplet1 = Droplet1.new(
  destroyed_at: DateTimeHelper.from_rfc3339('2020-04-01T18:11:49Z'),
  error_message: 'error_message0',
  id: '61486916',
  name: 'ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



