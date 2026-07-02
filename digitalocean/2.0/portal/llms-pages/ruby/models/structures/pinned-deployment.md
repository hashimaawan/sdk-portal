# Pinned Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlBpbm5lZERlcGxveW1lbnQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`PinnedDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cause` | `String` | Optional | - |
| `cloned_from` | `String` | Optional | - |
| `created_at` | `DateTime` | Optional | - |
| `functions` | [`Array[FunctionsComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - |
| `id` | `String` | Optional | - |
| `jobs` | [`Array[JobComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - |
| `phase` | [`Phase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/phase.md) | Optional | **Default**: `Phase::UNKNOWN` |
| `phase_last_updated_at` | `DateTime` | Optional | - |
| `progress` | [`Progress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/progress.md) | Optional | - |
| `services` | [`Array[ServiceComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `static_sites` | [`Array[StaticSiteComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - |
| `tier_slug` | `String` | Optional, Read-only | - |
| `updated_at` | `DateTime` | Optional | - |
| `workers` | [`Array[WorkerComponentsThatArePartOfThisDeployment]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
pinned_deployment = PinnedDeployment.new(
  cause: 'commit 9a4df0b pushed to github/digitalocean/sample-golang',
  cloned_from: '3aa4d20e-5527-4c00-b496-601fbd22520a',
  created_at: DateTimeHelper.from_rfc3339('2020-07-28T18:00:00Z'),
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
  id: 'b6bdf840-2854-4f87-a36c-5f231c617c84',
  phase: Phase::ACTIVE,
  phase_last_updated_at: DateTimeHelper.from_rfc3339('0001-01-01T00:00:00Z'),
  tier_slug: 'basic',
  updated_at: DateTimeHelper.from_rfc3339('2020-07-28T18:00:00Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



