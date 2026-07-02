# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projects` | [`Array[Project]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/project.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_projects_response = V2ProjectsResponse.new(
  meta: Meta.new(
    total: 2,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  projects: [
    Project.new(
      created_at: DateTimeHelper.from_rfc3339('2018-09-27T20:10:35Z'),
      description: 'My website API',
      environment: Environment::PRODUCTION,
      id: '4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679',
      name: 'my-web-api',
      owner_id: 258992,
      owner_uuid: '99525febec065ca37b2ffe4f852fd2b2581895e7',
      purpose: 'Service or API',
      updated_at: DateTimeHelper.from_rfc3339('2018-09-27T20:10:35Z'),
      is_default: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Project.new(
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
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'https://api.digitalocean.com/v2/projects?page=1',
      mnext: 'next2',
      additional_properties: {
        'first' => JSON.parse('"https://api.digitalocean.com/v2/projects?page=1"')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



