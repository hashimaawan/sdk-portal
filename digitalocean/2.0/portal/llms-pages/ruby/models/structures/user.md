# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlVzZXI

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mysql_settings` | [`MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mysql-settings.md) | Optional | - |
| `name` | `String` | Required | The name of a database user. |
| `password` | `String` | Optional, Read-only | A randomly generated password for the database user. |
| `role` | [`Role`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/role.md) | Optional, Read-only | A string representing the database user's role. The value will be either<br>"primary" or "normal". |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
user = User.new(
  name: 'app-01',
  mysql_settings: MysqlSettings.new(
    auth_plugin: AuthPlugin::MYSQL_NATIVE_PASSWORD,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  password: 'jge5lfxtzhx42iff',
  role: Role::NORMAL,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



