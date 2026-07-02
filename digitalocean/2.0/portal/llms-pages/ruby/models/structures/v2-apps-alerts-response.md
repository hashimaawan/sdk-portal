# V2 Apps Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsAlertsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`Array[Alert1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/alert-1.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_alerts_response = V2AppsAlertsResponse.new(
  alerts: [
    Alert1.new(
      component_name: 'component_name6',
      emails: [
        'emails5',
        'emails6'
      ],
      id: 'id6',
      phase: Phase1::ACTIVE,
      progress: Progress2.new(
        steps: [
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Alert1.new(
      component_name: 'component_name6',
      emails: [
        'emails5',
        'emails6'
      ],
      id: 'id6',
      phase: Phase1::ACTIVE,
      progress: Progress2.new(
        steps: [
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Alert1.new(
      component_name: 'component_name6',
      emails: [
        'emails5',
        'emails6'
      ],
      id: 'id6',
      phase: Phase1::ACTIVE,
      progress: Progress2.new(
        steps: [
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          StepsOfAnAlertSProgress.new(
            ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            name: 'name2',
            reason: Reason.new(
              code: 'code2',
              message: 'message4',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
            status: Status2::SUCCESS,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



