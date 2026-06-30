# Followers Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkZvbGxvd2Vyc09iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`FollowersObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Optional | This will always be set to null, as the Web API does not support it at the moment. |
| `total` | `Integer` | Optional | The total number of followers. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
followers_object = FollowersObject.new(
  href: 'href8',
  total: 198,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



