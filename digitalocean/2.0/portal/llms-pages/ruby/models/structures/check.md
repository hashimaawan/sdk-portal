# Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoZWNr

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Check`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `UUID \| String` | Optional, Read-only | A unique ID that can be used to identify and reference the check. |
| `enabled` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` |
| `name` | `String` | Optional | A human-friendly display name. |
| `regions` | [`Array[Region8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. |
| `target` | `String` | Optional | The endpoint to perform healthchecks on. |
| `type` | [`Type19`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-19.md) | Optional | The type of health check to perform. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
check = Check.new(
  id: '5a4981aa-9653-4bd1-bef5-d6bff52042e4',
  enabled: true,
  name: 'Landing page check',
  regions: [
    Region8::US_EAST,
    Region8::EU_WEST
  ],
  target: 'https://www.landingpage.com',
  type: Type19::HTTPS,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



