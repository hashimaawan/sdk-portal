# V2 Functions Namespaces Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespaces` | [`Array[Namespace]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/namespace.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_functions_namespaces_response = V2FunctionsNamespacesResponse.new(
  namespaces: [
    Namespace.new(
      api_host: 'api_host8',
      created_at: 'created_at0',
      key: 'key2',
      label: 'label2',
      namespace: 'namespace0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



