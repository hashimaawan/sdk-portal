# External Id Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkV4dGVybmFsSWRPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`ExternalIdObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isrc` | `String` | Optional | [International Standard Recording Code](http://en.wikipedia.org/wiki/International_Standard_Recording_Code) |
| `ean` | `String` | Optional | [International Article Number](http://en.wikipedia.org/wiki/International_Article_Number_%28EAN%29) |
| `upc` | `String` | Optional | [Universal Product Code](http://en.wikipedia.org/wiki/Universal_Product_Code) |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
external_id_object = ExternalIdObject.new(
  isrc: 'isrc8',
  ean: 'ean8',
  upc: 'upc2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



