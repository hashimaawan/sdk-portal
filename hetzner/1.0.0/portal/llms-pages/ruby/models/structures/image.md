# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type Object.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bound_to` | `Integer` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `created_from` | [`CreatedFrom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/created-from.md) | Required | Information about the Server the Image was created from |
| `deleted` | `String` | Required | Point in time where the Image was deleted (in ISO-8601 format) |
| `deprecated` | `String` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) |
| `description` | `String` | Required | Description of the Image |
| `disk_size` | `Float` | Required | Size of the disk contained in the Image in GB |
| `id` | `Integer` | Required | ID of the Resource |
| `image_size` | `Float` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Unique identifier of the Image. This value is only set for system Images. |
| `os_flavor` | [`OsFlavor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image |
| `os_version` | `String` | Required | Operating system version |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `rapid_deploy` | `TrueClass \| FalseClass` | Optional | Indicates that rapid deploy of the Image is available |
| `status` | [`Status24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable |
| `type` | [`Type22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-22.md) | Required | Type of the Image |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
image = Image.new(
  bound_to: nil,
  created: '2016-01-30T23:55:00+00:00',
  created_from: CreatedFrom.new(
    id: 1,
    name: 'Server',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  deleted: nil,
  deprecated: '2018-02-28T00:00:00+00:00',
  description: 'Ubuntu 20.04 Standard 64 bit',
  disk_size: 10,
  id: 42,
  image_size: 2.3,
  labels: {
    'key0' => 'labels4'
  },
  name: 'ubuntu-20.04',
  os_flavor: OsFlavor::UBUNTU,
  os_version: '20.04',
  protection: Protection.new(
    delete: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  status: Status24::UNAVAILABLE,
  type: Type22::SNAPSHOT,
  rapid_deploy: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



