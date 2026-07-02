# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `check_name` | `String` | Optional | The clusterlint check that resulted in the diagnostic. |
| `message` | `String` | Optional | Feedback about the object for users to fix. |
| `object` | [`Object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. |
| `severity` | `String` | Optional | Can be one of error, warning or suggestion. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
diagnostic = Diagnostic.new(
  check_name: 'unused-config-map',
  message: 'Unused config map',
  object: Object.new(
    kind: 'kind0',
    name: 'name2',
    namespace: 'namespace0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  severity: 'warning',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



