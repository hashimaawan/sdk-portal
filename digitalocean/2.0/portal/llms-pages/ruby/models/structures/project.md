# Project

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb2plY3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Project`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `description` | `String` | Optional | The description of the project. The maximum length is 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` |
| `environment` | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/environment.md) | Optional | The environment of the project's resources. |
| `id` | `UUID \| String` | Optional, Read-only | The unique universal identifier of this project. |
| `name` | `String` | Optional | The human-readable name for the project. The maximum length is 175 characters and the name must be unique.<br><br>**Constraints**: *Maximum Length*: `175` |
| `owner_id` | `Integer` | Optional, Read-only | The integer id of the project owner. |
| `owner_uuid` | `String` | Optional, Read-only | The unique universal identifier of the project owner. |
| `purpose` | `String` | Optional | The purpose of the project. The maximum length is 255 characters. It can<br>have one of the following values:<br><br>- Just trying out DigitalOcean<br>- Class project / Educational purposes<br>- Website or blog<br>- Web Application<br>- Service or API<br>- Mobile Application<br>- Machine learning / AI / Data processing<br>- IoT<br>- Operational / Developer tooling<br><br>If another value for purpose is specified, for example, "your custom purpose",<br>your purpose will be stored as `Other: your custom purpose`.<br><br>**Constraints**: *Maximum Length*: `255` |
| `updated_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was updated. |
| `is_default` | `TrueClass \| FalseClass` | Optional | If true, all resources will be added to this project if no project is specified. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
project = Project.new(
  created_at: DateTimeHelper.from_rfc3339('2018-09-27T20:10:35Z'),
  description: 'My website API',
  environment: Environment::PRODUCTION,
  id: '4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679',
  name: 'my-web-api',
  owner_id: 258992,
  owner_uuid: '99525febec065ca37b2ffe4f852fd2b2581895e7',
  purpose: 'Service or API',
  updated_at: DateTimeHelper.from_rfc3339('2018-09-27T20:10:35Z'),
  is_default: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



