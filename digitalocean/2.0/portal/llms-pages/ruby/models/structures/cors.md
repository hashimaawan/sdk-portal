# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Cors`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_credentials` | `TrueClass \| FalseClass` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. |
| `allow_headers` | `Array[String]` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. |
| `allow_methods` | `Array[String]` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. |
| `allow_origins` | [`Array[AllowOrigin]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. |
| `expose_headers` | `Array[String]` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. |
| `max_age` | `String` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
cors = Cors.new(
  allow_credentials: false,
  allow_headers: [
    'Content-Type',
    'X-Custom-Header'
  ],
  allow_methods: [
    'GET',
    'OPTIONS',
    'POST',
    'PUT',
    'PATCH',
    'DELETE'
  ],
  allow_origins: [
    AllowOrigin.new(
      exact: 'https://www.example.com',
      prefix: 'prefix6',
      regex: 'regex4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AllowOrigin.new(
      exact: 'exact8',
      prefix: 'prefix6',
      regex: '^.*example.com',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  expose_headers: [
    'Content-Encoding',
    'X-Custom-Header'
  ],
  max_age: '5h30m',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



