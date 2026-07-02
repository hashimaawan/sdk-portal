# Scheduled Details

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNjaGVkdWxlZERldGFpbHM

Trigger details for SCHEDULED type, where body is optional.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ScheduledDetails`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Body`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/body.md) | Optional | Optional data to be sent to function while triggering the function. |
| `cron` | `String` | Required | valid cron expression string which is required for SCHEDULED type triggers. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
scheduled_details = ScheduledDetails.new(
  cron: '* * * * *',
  body: Body.new(
    name: 'name6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



