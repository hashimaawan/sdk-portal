# V2 Kubernetes Clusters Clusterlint Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `run_id` | `String` | Optional | ID of the clusterlint run that can be used later to fetch the diagnostics. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_clusterlint_response1 = V2KubernetesClustersClusterlintResponse1.new(
  run_id: '50c2f44c-011d-493e-aee5-361a4a0d1844',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



