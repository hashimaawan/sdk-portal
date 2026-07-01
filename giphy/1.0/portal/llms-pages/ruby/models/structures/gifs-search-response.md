# Gifs Search Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdpZnMlMjUyMFNlYXJjaCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`GifsSearchResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Array[Gif]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
gifs_search_response = GifsSearchResponse.new(
  data: [
    Gif.new(
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
    Gif.new(
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
    )
  ],
  meta: Meta.new(
    msg: 'msg8',
    response_id: 'response_id0',
    status: 98,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  pagination: Pagination.new(
    count: 192,
    offset: 240,
    total_count: 100,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



