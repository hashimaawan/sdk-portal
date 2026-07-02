# Mysql Settings

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk15c3FsU2V0dGluZ3M

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`MysqlSettings`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auth_plugin` | [`AuthPlugin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/auth-plugin.md) | Required | A string specifying the authentication method to be used for connections<br>to the MySQL user account. The valid values are `mysql_native_password`<br>or `caching_sha2_password`. If excluded when creating a new user, the<br>default for the version of MySQL in use will be used. As of MySQL 8.0, the<br>default is `caching_sha2_password`. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
mysql_settings = MysqlSettings.new(
  auth_plugin: AuthPlugin::MYSQL_NATIVE_PASSWORD,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



