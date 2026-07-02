# V2 Projects Default Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project` | [`Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/project.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_projects_default_response = V2ProjectsDefaultResponse.new(
  project: Project.new(
    created_at: DateTimeHelper.from_rfc3339('2017-10-19T21:44:20Z'),
    description: 'Default project',
    environment: Environment::DEVELOPMENT,
    id: 'addb4547-6bab-419a-8542-76263a033cf6',
    name: 'Default',
    owner_id: 258992,
    owner_uuid: '99525febec065ca37b2ffe4f852fd2b2581895e7',
    purpose: 'Just trying out DigitalOcean',
    updated_at: DateTimeHelper.from_rfc3339('2019-11-05T18:50:03Z'),
    is_default: true,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



