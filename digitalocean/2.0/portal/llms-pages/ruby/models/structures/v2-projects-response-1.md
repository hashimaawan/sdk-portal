# V2 Projects Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ProjectsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project` | [`Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/project.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_projects_response1 = V2ProjectsResponse1.new(
  project: Project.new(
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    description: 'description4',
    environment: Environment::DEVELOPMENT,
    id: '000026e4-0000-0000-0000-000000000000',
    name: 'name6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



