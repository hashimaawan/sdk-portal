# Saved Show Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlNhdmVkU2hvd09iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`SavedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `DateTime` | Optional | The date and time the show was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `show` | [`ShowBase`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/show-base.md) | Optional | Information about the show. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
saved_show_object = SavedShowObject.new(
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
```



