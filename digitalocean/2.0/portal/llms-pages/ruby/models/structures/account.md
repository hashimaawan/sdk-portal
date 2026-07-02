# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Account`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_limit` | `Integer` | Required | The total number of Droplets current user or team may have active at one time. |
| `email` | `String` | Required | The email address used by the current user to register for DigitalOcean. |
| `email_verified` | `TrueClass \| FalseClass` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `false` |
| `floating_ip_limit` | `Integer` | Required | The total number of Floating IPs the current user or team may have. |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `Status::ACTIVE` |
| `status_message` | `String` | Required | A human-readable message giving more details about the status of the account. |
| `team` | [`Team`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. |
| `uuid` | `String` | Required | The unique universal identifier for the current user. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
account = Account.new(
  droplet_limit: 25,
  email: 'sammy@digitalocean.com',
  email_verified: true,
  floating_ip_limit: 5,
  status: Status::ACTIVE,
  status_message: ' ',
  uuid: 'b6fr89dbf6d9156cace5f3c78dc9851d957381ef',
  team: Team.new(
    name: 'name0',
    uuid: 'uuid6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



