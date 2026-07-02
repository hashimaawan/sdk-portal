# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Namespace`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `api_host` | `String` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. |
| `created_at` | `String` | Optional | UTC time string. |
| `key` | `String` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. |
| `label` | `String` | Optional | The namespace's unique name. |
| `namespace` | `String` | Optional | A unique string format of UUID with a prefix fn-. |
| `region` | `String` | Optional | The namespace's datacenter region. |
| `updated_at` | `String` | Optional | UTC time string. |
| `uuid` | `String` | Optional | The namespace's Universally Unique Identifier. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
namespace = Namespace.new(
  api_host: 'https://api_host.io',
  created_at: '2022-09-14T04:16:45Z',
  key: 'd1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2',
  label: 'my namespace',
  namespace: 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
  region: 'nyc1',
  updated_at: '2022-09-14T04:16:45Z',
  uuid: 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



