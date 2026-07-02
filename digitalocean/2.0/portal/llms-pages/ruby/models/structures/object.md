# Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk9iamVjdA

Metadata about the Kubernetes API object the diagnostic is reported on.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Object`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kind` | `String` | Optional | The kind of Kubernetes API object |
| `name` | `String` | Optional | Name of the object |
| `namespace` | `String` | Optional | The namespace the object resides in the cluster. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
object = Object.new(
  kind: 'config map',
  name: 'foo',
  namespace: 'kube-system',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



