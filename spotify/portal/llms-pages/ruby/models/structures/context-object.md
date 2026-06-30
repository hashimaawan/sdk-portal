# Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkNvbnRleHRPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`ContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `String` | Optional | The object type, e.g. "artist", "playlist", "album", "show". |
| `href` | `String` | Optional | A link to the Web API endpoint providing full details of the track. |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Optional | External URLs for this context. |
| `uri` | `String` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the context. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
context_object = ContextObject.new(
  type: 'type0',
  href: 'href2',
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  uri: 'uri4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



