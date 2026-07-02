# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `continent` | `String` | Optional, Read-only | - |
| `data_centers` | `Array[String]` | Optional, Read-only | - |
| `default` | `TrueClass \| FalseClass` | Optional, Read-only | Whether or not the region is presented as the default. |
| `disabled` | `TrueClass \| FalseClass` | Optional, Read-only | - |
| `flag` | `String` | Optional, Read-only | - |
| `label` | `String` | Optional, Read-only | - |
| `reason` | `String` | Optional, Read-only | - |
| `slug` | `String` | Optional, Read-only | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
geographical_information_about_an_app_origin = GeographicalInformationAboutAnAppOrigin.new(
  continent: 'europe',
  data_centers: [
    'ams'
  ],
  default: true,
  disabled: true,
  flag: 'ams',
  label: 'ams',
  reason: 'to crowded',
  slug: 'basic',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



