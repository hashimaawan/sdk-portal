# Gifs Translate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdpZnMlMjUyMFRyYW5zbGF0ZSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`GifsTranslateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
gifs_translate_response = GifsTranslateResponse.new(
  data: Gif.new(
    bitly_url: 'bitly_url0',
    content_url: 'content_url4',
    create_datetime: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    embded_url: 'embded_url8',
    featured_tags: [
      'featured_tags0'
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  meta: Meta.new(
    msg: 'msg8',
    response_id: 'response_id0',
    status: 98,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



