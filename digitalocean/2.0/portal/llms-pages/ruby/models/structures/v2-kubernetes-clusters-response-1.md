# V2 Kubernetes Clusters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_cluster` | [`KubernetesCluster`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/kubernetes-cluster.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_response1 = V2KubernetesClustersResponse1.new(
  kubernetes_cluster: KubernetesCluster.new(
    name: 'name8',
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
      )
    ],
    region: 'region4',
    version: 'version4',
    auto_upgrade: false,
    cluster_subnet: 'cluster_subnet0',
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    endpoint: 'endpoint6',
    ha: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



