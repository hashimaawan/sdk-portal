# Status 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXR1czEx

An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Status11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `String` | Optional | An optional message providing additional information about the current cluster state. |
| `state` | [`State2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/state-2.md) | Optional | A string indicating the current status of the cluster. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
status11 = Status11.new(
  message: 'provisioning',
  state: State2::PROVISIONING,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



