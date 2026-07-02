# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/image-1.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_images_response2 = V2ImagesResponse2.new(
  image: Image1.new(
    created_at: DateTimeHelper.from_rfc3339('2020-05-04T22:23:02Z'),
    description: 'description6',
    distribution: Distribution::UBUNTU,
    error_message: 'error_message8',
    id: 7555620,
    min_disk_size: 20,
    name: 'Nifty New Snapshot',
    public: true,
    regions: [
      Region2::NYC1,
      Region2::NYC2
    ],
    size_gigabytes: 2.34,
    slug: 'nifty1',
    status: Status7::NEW,
    tags: [
      'base-image',
      'prod'
    ],
    type: Type9::SNAPSHOT,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



