# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `msg` | `String` | Optional | HTTP Response Message |
| `response_id` | `String` | Optional | A unique ID paired with this response from the API. |
| `status` | `Integer` | Optional | HTTP Response Code |


# Example

```ruby
meta = Meta.new(
  'OK',
  '57eea03c72381f86e05c35d2',
  200
)
```



