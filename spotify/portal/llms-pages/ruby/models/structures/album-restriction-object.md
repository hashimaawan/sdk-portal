# Album Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkFsYnVtUmVzdHJpY3Rpb25PYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`AlbumRestrictionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/enumerations/reason.md) | Optional | The reason for the restriction. Albums may be restricted if the content is not available in a given market, to the user's subscription type, or when the user's account is set to not play explicit content.<br>Additional reasons may be added in the future. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
album_restriction_object = AlbumRestrictionObject.new(
  reason: Reason::MARKET,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



