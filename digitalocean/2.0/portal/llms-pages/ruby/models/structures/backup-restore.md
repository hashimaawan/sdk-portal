# Backup Restore

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhY2t1cFJlc3RvcmU

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`BackupRestore`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backup_created_at` | `DateTime` | Optional | The timestamp of an existing database cluster backup in ISO8601 combined date and time format. The most recent backup will be used if excluded. |
| `database_name` | `String` | Required | The name of an existing database cluster from which the backup will be restored. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
backup_restore = BackupRestore.new(
  database_name: 'backend',
  backup_created_at: DateTimeHelper.from_rfc3339('2019-01-31T19:25:22Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



