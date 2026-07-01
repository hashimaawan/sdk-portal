# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.

*This model accepts additional fields of type Object.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `msg` | `String` | Optional | HTTP Response Message |
| `response_id` | `String` | Optional | A unique ID paired with this response from the API. |
| `status` | `Integer` | Optional | HTTP Response Code |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
meta = Meta.new(
  msg: 'OK',
  response_id: '57eea03c72381f86e05c35d2',
  status: 200,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



