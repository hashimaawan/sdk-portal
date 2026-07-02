# V2 Kubernetes Clusters Clusterlint Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `exclude_checks` | `Array[String]` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `exclude_groups` | `Array[String]` | Optional | An array of check groups that will be omitted when clusterlint executes checks. |
| `include_checks` | `Array[String]` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `include_groups` | `Array[String]` | Optional | An array of check groups that will be run when clusterlint executes checks. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_clusterlint_request = V2KubernetesClustersClusterlintRequest.new(
  exclude_checks: [
    'default-namespace'
  ],
  exclude_groups: [
    'workload-health'
  ],
  include_checks: [
    'bare-pods',
    'resource-requirements'
  ],
  include_groups: [
    'basic',
    'doks',
    'security'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



