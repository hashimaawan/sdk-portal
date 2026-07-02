# V2 Projects Default Resources Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResourcesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`Array[Resources1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/resources-1.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_projects_default_resources_response1 = V2ProjectsDefaultResourcesResponse1.new(
  resources: [
    Resources1.new(
      assigned_at: DateTimeHelper.from_rfc3339('2018-09-28T19:26:37Z'),
      links: Links4.new(
        mself: 'https://api.digitalocean.com/v2/droplets/13457723',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      status: Status14::OK,
      urn: 'do:droplet:13457723',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Resources1.new(
      assigned_at: DateTimeHelper.from_rfc3339('2019-03-31T16:24:14Z'),
      links: Links4.new(
        mself: 'https://api.digitalocean.com/v2/domains/example.com',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      status: Status14::OK,
      urn: 'do:domain:example.com',
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



