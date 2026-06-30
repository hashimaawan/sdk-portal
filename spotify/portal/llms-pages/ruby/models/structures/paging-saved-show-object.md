# Paging Saved Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkU2hvd09iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`PagingSavedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[SavedShowObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/saved-show-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_saved_show_object = PagingSavedShowObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    SavedShowObject.new(
      added_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      show: ShowBase.new(
        available_markets: [
          'available_markets0',
          'available_markets1',
          'available_markets2'
        ],
        copyrights: [
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          CopyrightObject.new(
            text: 'text2',
            type: 'type2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        description: 'description4',
        html_description: 'html_description4',
        explicit: false,
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'href8',
        id: 'id6',
        images: [
          ImageObject.new(
            url: 'url6',
            height: 182,
            width: 222,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          ImageObject.new(
            url: 'url6',
            height: 182,
            width: 222,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          ImageObject.new(
            url: 'url6',
            height: 182,
            width: 222,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        is_externally_hosted: false,
        languages: [
          'languages7',
          'languages6',
          'languages5'
        ],
        media_type: 'media_type6',
        name: 'name6',
        publisher: 'publisher6',
        type: 'type4',
        uri: 'uri0',
        total_episodes: 198,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
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



