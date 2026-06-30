# Many Simplified Shows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRk1hbnlTaW1wbGlmaWVkU2hvd3M

*This model accepts additional fields of type Object.*


# Class Name

`ManySimplifiedShows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `shows` | [`Array[ShowBase]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/show-base.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
many_simplified_shows = ManySimplifiedShows.new(
  shows: [
    ShowBase.new(
      available_markets: [
        'available_markets2'
      ],
      copyrights: [
        CopyrightObject.new(
          text: 'text2',
          type: 'type2',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      description: 'description8',
      html_description: 'html_description2',
      explicit: false,
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href0',
      id: 'id8',
      images: [
        ImageObject.new(
          url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
          height: 300,
          width: 300,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      is_externally_hosted: false,
      languages: [
        'languages5'
      ],
      media_type: 'media_type4',
      name: 'name8',
      publisher: 'publisher4',
      type: 'show',
      uri: 'uri2',
      total_episodes: 196,
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



