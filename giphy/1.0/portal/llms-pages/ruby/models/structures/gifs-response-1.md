# Gifs Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdpZnMlMjUyMFJlc3BvbnNlMQ


# Class Name

`GifsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |


# Example

```ruby
gifs_response1 = GifsResponse1.new(
  Gif.new(
    'bitly_url0',
    'content_url4',
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    'embded_url8',
    [
      'featured_tags0'
    ],
    nil,
    Images.new(
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new,
      Image.new
    ),
    DateTimeHelper.from_rfc3339(nil),
    nil,
    nil,
    nil,
    nil,
    nil,
    [],
    DateTimeHelper.from_rfc3339(nil),
    envrr,
    DateTimeHelper.from_rfc3339(nil),
    nil,
    User.new
  ),
  Meta.new(
    'msg8',
    'response_id0',
    98
  )
)
```



