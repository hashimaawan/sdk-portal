# A Step that Is Run as Part of the Deployment S Lifecycle

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkElMjUyMHN0ZXAlMjUyMHRoYXQlMjUyMGlzJTI1MjBydW4lMjUyMGFzJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhlJTI1MjBkZXBsb3ltZW50JTI1MjdzJTI1MjBsaWZlY3ljbGU

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AStepThatIsRunAsPartOfTheDeploymentSLifecycle`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `component_name` | `String` | Optional | - |
| `ended_at` | `DateTime` | Optional | - |
| `message_base` | `String` | Optional | The base of a human-readable description of the step intended to be combined with the component name for presentation. For example:<br><br>`message_base` = "Building service"<br>`component_name` = "api" |
| `name` | `String` | Optional | - |
| `reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/reason.md) | Optional | - |
| `started_at` | `DateTime` | Optional | - |
| `status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-2.md) | Optional | **Default**: `Status2::UNKNOWN` |
| `steps` | [`Array[Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
a_step_that_is_run_as_part_of_the_deployment_s_lifecycle = AStepThatIsRunAsPartOfTheDeploymentSLifecycle.new(
  component_name: 'component',
  ended_at: DateTimeHelper.from_rfc3339('2020-11-19T20:27:18Z'),
  message_base: 'Building service',
  name: 'example_step',
  reason: Reason.new(
    code: 'code2',
    message: 'message4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  started_at: DateTimeHelper.from_rfc3339('2020-11-19T20:27:18Z'),
  status: Status2::SUCCESS,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



