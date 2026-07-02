# V2 Kubernetes Clusters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_clusters` | [`Array[KubernetesCluster]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/kubernetes-cluster.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_response = V2KubernetesClustersResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  kubernetes_clusters: [
    KubernetesCluster.new(
      name: 'name2',
      node_pools: [
        NodePool.new(
          size: 'size6',
          count: 206,
          name: 'name4',
          auto_scale: false,
          id: '000013be-0000-0000-0000-000000000000',
          labels: { 'key1' => 'val1', 'key2' => 'val2' },
          max_nodes: 118,
          min_nodes: 54,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        NodePool.new(
          size: 'size6',
          count: 206,
          name: 'name4',
          auto_scale: false,
          id: '000013be-0000-0000-0000-000000000000',
          labels: { 'key1' => 'val1', 'key2' => 'val2' },
          max_nodes: 118,
          min_nodes: 54,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        NodePool.new(
          size: 'size6',
          count: 206,
          name: 'name4',
          auto_scale: false,
          id: '000013be-0000-0000-0000-000000000000',
          labels: { 'key1' => 'val1', 'key2' => 'val2' },
          max_nodes: 118,
          min_nodes: 54,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      region: 'region8',
      version: 'version8',
      auto_upgrade: false,
      cluster_subnet: 'cluster_subnet4',
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      endpoint: 'endpoint0',
      ha: false,
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



