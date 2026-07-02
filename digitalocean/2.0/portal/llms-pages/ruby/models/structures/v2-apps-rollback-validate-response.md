# V2 Apps Rollback Validate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwVmFsaWRhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsRollbackValidateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/error.md) | Optional | - |
| `valid` | `TrueClass \| FalseClass` | Optional | Indicates whether the app can be rolled back to the specified deployment. |
| `warnings` | [`Array[Warning]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/warning.md) | Optional | Contains a list of warnings that may cause the rollback to run under unideal circumstances. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_rollback_validate_response = V2AppsRollbackValidateResponse.new(
  error: Error.new(
    code: Code::INCOMPATIBLE_PHASE,
    components: [
      'components3'
    ],
    message: 'message4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  valid: false,
  warnings: [
    Warning.new(
      code: Code::EXCEEDED_REVISION_LIMIT,
      components: [
        'components3'
      ],
      message: 'message4',
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



