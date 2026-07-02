# V2 Kubernetes Clusters Upgrade Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUpgradeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | `String` | Optional | The slug identifier for the version of Kubernetes that the cluster will be upgraded to. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_upgrade_request = V2KubernetesClustersUpgradeRequest.new(
  version: '1.16.13-do.0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



