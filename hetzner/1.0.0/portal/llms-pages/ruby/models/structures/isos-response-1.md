# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/iso.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
isos_response1 = IsosResponse1.new(
  iso: Iso.new(
    deprecated: '2018-02-28T00:00:00+00:00',
    description: 'FreeBSD 11.0 x64',
    id: 42,
    name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
    type: Type26::PUBLIC,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



