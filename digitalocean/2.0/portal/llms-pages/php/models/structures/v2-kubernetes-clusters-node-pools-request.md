# V2 Kubernetes Clusters Node Pools Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autoScale` | `?bool` | Optional | A boolean value indicating whether auto-scaling is enabled for this node pool. | getAutoScale(): ?bool | setAutoScale(?bool autoScale): void |
| `count` | `?int` | Optional | The number of Droplet instances in the node pool. | getCount(): ?int | setCount(?int count): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a specific node pool. | getId(): ?string | setId(?string id): void |
| `labels` | [`?array`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | An object containing a set of Kubernetes labels. The keys and are values are both user-defined. | getLabels(): ?array | setLabels(?array labels): void |
| `maxNodes` | `?int` | Optional | The maximum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. | getMaxNodes(): ?int | setMaxNodes(?int maxNodes): void |
| `minNodes` | `?int` | Optional | The minimum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. | getMinNodes(): ?int | setMinNodes(?int minNodes): void |
| `name` | `?string` | Optional | A human-readable name for the node pool. | getName(): ?string | setName(?string name): void |
| `nodes` | [`?(Node[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/node.md) | Optional, Read-only | An object specifying the details of a specific worker node in a node pool. | getNodes(): ?array | setNodes(?array nodes): void |
| `tags` | `?(string[])` | Optional | An array containing the tags applied to the node pool. All node pools are automatically tagged `k8s`, `k8s-worker`, and `k8s:$K8S_CLUSTER_ID`. | getTags(): ?array | setTags(?array tags): void |
| `taints` | [`?(Taint[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/taint.md) | Optional | An array of taints to apply to all nodes in a pool. Taints will automatically be applied to all existing nodes and any subsequent nodes added to the pool. When a taint is removed, it is removed from all nodes in the pool. | getTaints(): ?array | setTaints(?array taints): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersNodePoolsRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersNodePoolsRequest = V2KubernetesClustersNodePoolsRequestBuilder::init()
    ->autoScale(true)
    ->count(3)
    ->id('cdda885e-7663-40c8-bc74-3a036c66545d')
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->maxNodes(6)
    ->minNodes(3)
    ->name('frontend-pool')
    ->tags(
        [
            'k8s',
            'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
            'k8s-worker',
            'production',
            'web-team'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



