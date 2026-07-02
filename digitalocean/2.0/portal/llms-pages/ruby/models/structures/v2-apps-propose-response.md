# V2 Apps Propose Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsProposeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_cost` | `Integer` | Optional | The monthly cost of the proposed app in USD using the next pricing plan tier. For example, if you propose an app that uses the Basic tier, the `app_tier_upgrade_cost` field displays the monthly cost of the app if it were to use the Professional tier. If the proposed app already uses the most expensive tier, the field is empty. |
| `app_is_static` | `TrueClass \| FalseClass` | Optional | Indicates whether the app is a static app. |
| `app_name_available` | `TrueClass \| FalseClass` | Optional | Indicates whether the app name is available. |
| `app_name_suggestion` | `String` | Optional | The suggested name if the proposed app name is unavailable. |
| `app_tier_downgrade_cost` | `Integer` | Optional | The monthly cost of the proposed app in USD using the previous pricing plan tier. For example, if you propose an app that uses the Professional tier, the `app_tier_downgrade_cost` field displays the monthly cost of the app if it were to use the Basic tier. If the proposed app already uses the lest expensive tier, the field is empty. |
| `existing_static_apps` | `String` | Optional | The maximum number of free static apps the account can have. We will charge you for any additional static apps. |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_propose_response = V2AppsProposeResponse.new(
  app_cost: 5,
  app_is_static: true,
  app_name_available: true,
  app_name_suggestion: 'newName',
  app_tier_downgrade_cost: 17,
  existing_static_apps: '2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



