# Configurations for External Logging

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25zJTI1MjBmb3IlMjUyMGV4dGVybmFsJTI1MjBsb2dnaW5nLg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ConfigurationsForExternalLogging`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datadog` | [`Datadog`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/datadog.md) | Optional | DataDog configuration. |
| `logtail` | [`Logtail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/logtail.md) | Optional | Logtail configuration. |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `2`, *Maximum Length*: `42`, *Pattern*: `^[A-Za-z0-9()\[\]'"][-A-Za-z0-9_. \/()\[\]]{0,40}[A-Za-z0-9()\[\]'"]$` |
| `papertrail` | [`Papertrail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/papertrail.md) | Optional | Papertrail configuration. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
configurations_for_external_logging = ConfigurationsForExternalLogging.new(
  name: 'my_log_destination',
  datadog: Datadog.new(
    api_key: 'api_key2',
    endpoint: 'endpoint8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  logtail: Logtail.new(
    token: 'token4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  papertrail: Papertrail.new(
    endpoint: 'endpoint4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



