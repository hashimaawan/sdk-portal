# Explicit Content Settings Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkV4cGxpY2l0Q29udGVudFNldHRpbmdzT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ExplicitContentSettingsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter_enabled` | `TrueClass \| FalseClass` | Optional | When `true`, indicates that explicit content should not be played. |
| `filter_locked` | `TrueClass \| FalseClass` | Optional | When `true`, indicates that the explicit content setting is locked and can't be changed by the user. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
explicit_content_settings_object = ExplicitContentSettingsObject.new(
  filter_enabled: false,
  filter_locked: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



