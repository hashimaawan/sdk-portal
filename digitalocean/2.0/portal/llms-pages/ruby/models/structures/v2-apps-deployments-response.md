# V2 Apps Deployments Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsDeploymentsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deployments` | [`Array[AnAppDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/an-app-deployment.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_deployments_response = V2AppsDeploymentsResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  deployments: [
    AnAppDeployment.new(
      cause: 'cause2',
      cloned_from: 'cloned_from4',
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      functions: [
        FunctionsComponentsThatArePartOfThisDeployment.new(
          name: 'name4',
          namespace: 'namespace8',
          source_commit_hash: 'source_commit_hash4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      id: 'id6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AnAppDeployment.new(
      cause: 'cause2',
      cloned_from: 'cloned_from4',
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      functions: [
        FunctionsComponentsThatArePartOfThisDeployment.new(
          name: 'name4',
          namespace: 'namespace8',
          source_commit_hash: 'source_commit_hash4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      id: 'id6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AnAppDeployment.new(
      cause: 'cause2',
      cloned_from: 'cloned_from4',
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      functions: [
        FunctionsComponentsThatArePartOfThisDeployment.new(
          name: 'name4',
          namespace: 'namespace8',
          source_commit_hash: 'source_commit_hash4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      id: 'id6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'last6',
      mnext: 'next2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
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



