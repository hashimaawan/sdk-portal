# Version Availability

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlZlcnNpb25BdmFpbGFiaWxpdHk

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`VersionAvailability`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mongodb` | [`Array[Mongodb1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `mysql` | [`Array[Mongodb1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `pg` | [`Array[Mongodb1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `redis` | [`Array[Mongodb1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
version_availability = VersionAvailability.new(
  mongodb: [
    Mongodb1.new(
      end_of_availability: 'end_of_availability4',
      end_of_life: 'end_of_life4',
      version: 'version4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Mongodb1.new(
      end_of_availability: 'end_of_availability4',
      end_of_life: 'end_of_life4',
      version: 'version4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  mysql: [
    Mongodb1.new(
      end_of_availability: 'end_of_availability0',
      end_of_life: 'end_of_life0',
      version: 'version0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Mongodb1.new(
      end_of_availability: 'end_of_availability0',
      end_of_life: 'end_of_life0',
      version: 'version0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  pg: [
    Mongodb1.new(
      end_of_availability: 'end_of_availability4',
      end_of_life: 'end_of_life4',
      version: 'version4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  redis: [
    Mongodb1.new(
      end_of_availability: 'end_of_availability8',
      end_of_life: 'end_of_life8',
      version: 'version8',
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



