# V2 Kubernetes Clusters Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

An object containing the IDs of resources associated with a Kubernetes cluster.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancers` | [`Array[LoadBalancer]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated load balancers that can be destroyed along with the cluster. |
| `volume_snapshots` | [`Array[LoadBalancer]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volume snapshots that can be destroyed along with the cluster. |
| `volumes` | [`Array[LoadBalancer]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volumes that can be destroyed along with the cluster. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_destroy_with_associated_resources_response = V2KubernetesClustersDestroyWithAssociatedResourcesResponse.new(
  load_balancers: [
    LoadBalancer.new(
      id: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
      name: 'lb-001',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  volume_snapshots: [
    LoadBalancer.new(
      id: 'edb0478d-7436-11ea-86e6-0a58ac144b91',
      name: 'snapshot-001',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  volumes: [
    LoadBalancer.new(
      id: 'ba49449a-7435-11ea-b89e-0a58ac14480f',
      name: 'volume-001',
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



