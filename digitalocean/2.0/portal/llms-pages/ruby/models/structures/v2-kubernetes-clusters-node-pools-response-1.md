# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `node_pool` | [`NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/node-pool.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_node_pools_response1 = V2KubernetesClustersNodePoolsResponse1.new(
  node_pool: NodePool.new(
    size: 's-1vcpu-2gb',
    count: 3,
    name: 'new-pool',
    auto_scale: true,
    id: 'cdda885e-7663-40c8-bc74-3a036c66545d',
    labels: nil,
    max_nodes: 6,
    min_nodes: 3,
    nodes: [
      Node.new(
        created_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z'),
        droplet_id: ' ',
        id: '478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f',
        name: ' ',
        status: Status10.new(
          state: State1::PROVISIONING
        ),
        updated_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z')
      ),
      Node.new(
        created_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z'),
        droplet_id: ' ',
        id: 'ad12e744-c2a9-473d-8aa9-be5680500eb1',
        name: ' ',
        status: Status10.new(
          state: State1::PROVISIONING
        ),
        updated_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z')
      ),
      Node.new(
        created_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z'),
        droplet_id: ' ',
        id: 'e46e8d07-f58f-4ff1-9737-97246364400e',
        name: ' ',
        status: Status10.new(
          state: State1::PROVISIONING
        ),
        updated_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z')
      )
    ],
    tags: [
      'production',
      'web-team',
      'front-end',
      'k8s',
      'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
      'k8s:worker'
    ],
    taints: [],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



