# State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXRlMw

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`State3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `previous_outage` | [`PreviousOutage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/previous-outage.md) | Optional | - |
| `regions` | [`Regions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/regions.md) | Optional | A map of region to regional state |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
state3 = State3.new(
  previous_outage: PreviousOutage.new(
    duration_seconds: 16,
    ended_at: 'ended_at4',
    region: 'region8',
    started_at: 'started_at4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  regions: Regions.new(
    eu_west: EuWest.new(
      status: Status16::DOWN,
      status_changed_at: 'status_changed_at4',
      thirty_day_uptime_percentage: 227.78,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    us_east: EuWest.new(
      status: Status16::DOWN,
      status_changed_at: 'status_changed_at4',
      thirty_day_uptime_percentage: 121.56,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



