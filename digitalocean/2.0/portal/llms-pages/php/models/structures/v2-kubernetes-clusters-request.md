# V2 Kubernetes Clusters Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autoUpgrade` | `?bool` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` | getAutoUpgrade(): ?bool | setAutoUpgrade(?bool autoUpgrade): void |
| `ha` | `?bool` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` | getHa(): ?bool | setHa(?bool ha): void |
| `maintenancePolicy` | [`?MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. | getMaintenancePolicy(): ?MaintenancePolicy | setMaintenancePolicy(?MaintenancePolicy maintenancePolicy): void |
| `name` | `string` | Required | A human-readable name for a Kubernetes cluster. | getName(): string | setName(string name): void |
| `surgeUpgrade` | `?bool` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` | getSurgeUpgrade(): ?bool | setSurgeUpgrade(?bool surgeUpgrade): void |
| `tags` | `?(string[])` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersRequestBuilder;
use DigitalOceanApiLib\Models\Builders\MaintenancePolicyBuilder;
use DigitalOceanApiLib\Models\Day;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersRequest = V2KubernetesClustersRequestBuilder::init(
    'prod-cluster-01'
)
    ->autoUpgrade(true)
    ->ha(true)
    ->maintenancePolicy(
        MaintenancePolicyBuilder::init()
            ->day(Day::ANY)
            ->duration('duration4')
            ->startTime('start_time2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->surgeUpgrade(true)
    ->tags(
        [
            'k8s',
            'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
            'production',
            'web-team'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



