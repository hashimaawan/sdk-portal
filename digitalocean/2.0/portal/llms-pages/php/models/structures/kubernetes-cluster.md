# Kubernetes Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVy

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`KubernetesCluster`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autoUpgrade` | `?bool` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` | getAutoUpgrade(): ?bool | setAutoUpgrade(?bool autoUpgrade): void |
| `clusterSubnet` | `?string` | Optional, Read-only | The range of IP addresses in the overlay network of the Kubernetes cluster in CIDR notation. | getClusterSubnet(): ?string | setClusterSubnet(?string clusterSubnet): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `endpoint` | `?string` | Optional, Read-only | The base URL of the API server on the Kubernetes master node. | getEndpoint(): ?string | setEndpoint(?string endpoint): void |
| `ha` | `?bool` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` | getHa(): ?bool | setHa(?bool ha): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a Kubernetes cluster. | getId(): ?string | setId(?string id): void |
| `ipv4` | `?string` | Optional, Read-only | The public IPv4 address of the Kubernetes master node. This will not be set if high availability is configured on the cluster (v1.21+) | getIpv4(): ?string | setIpv4(?string ipv4): void |
| `maintenancePolicy` | [`?MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. | getMaintenancePolicy(): ?MaintenancePolicy | setMaintenancePolicy(?MaintenancePolicy maintenancePolicy): void |
| `name` | `string` | Required | A human-readable name for a Kubernetes cluster. | getName(): string | setName(string name): void |
| `nodePools` | [`NodePool[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/node-pool.md) | Required | An object specifying the details of the worker nodes available to the Kubernetes cluster. | getNodePools(): array | setNodePools(array nodePools): void |
| `region` | `string` | Required | The slug identifier for the region where the Kubernetes cluster is located. | getRegion(): string | setRegion(string region): void |
| `registryEnabled` | `?bool` | Optional, Read-only | A read-only boolean value indicating if a container registry is integrated with the cluster. | getRegistryEnabled(): ?bool | setRegistryEnabled(?bool registryEnabled): void |
| `serviceSubnet` | `?string` | Optional, Read-only | The range of assignable IP addresses for services running in the Kubernetes cluster in CIDR notation. | getServiceSubnet(): ?string | setServiceSubnet(?string serviceSubnet): void |
| `status` | [`?Status11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/status-11.md) | Optional, Read-only | An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster. | getStatus(): ?Status11 | setStatus(?Status11 status): void |
| `surgeUpgrade` | `?bool` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` | getSurgeUpgrade(): ?bool | setSurgeUpgrade(?bool surgeUpgrade): void |
| `tags` | `?(string[])` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. | getTags(): ?array | setTags(?array tags): void |
| `updatedAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was last updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `version` | `string` | Required | The slug identifier for the version of Kubernetes used for the cluster. If set to a minor version (e.g. "1.14"), the latest version within it will be used (e.g. "1.14.6-do.1"); if set to "latest", the latest published version will be used. See the `/v2/kubernetes/options` endpoint to find all currently available versions. | getVersion(): string | setVersion(string version): void |
| `vpcUuid` | `?string` | Optional | A string specifying the UUID of the VPC to which the Kubernetes cluster is assigned. | getVpcUuid(): ?string | setVpcUuid(?string vpcUuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\KubernetesClusterBuilder;
use DigitalOceanApiLib\Models\Builders\NodePoolBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;

$kubernetesCluster = KubernetesClusterBuilder::init(
    'prod-cluster-01',
    [
        NodePoolBuilder::init(
            's-1vcpu-2gb',
            3,
            'frontend-pool'
        )
            ->autoScale(true)
            ->id('cdda885e-7663-40c8-bc74-3a036c66545d')
            ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->maxNodes(6)
            ->minNodes(3)
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
            ->build()
    ],
    'nyc1',
    '1.18.6-do.0'
)
    ->autoUpgrade(true)
    ->clusterSubnet('10.244.0.0/16')
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
    ->endpoint('https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com')
    ->ha(true)
    ->id('bd5f5959-5e1e-4205-a714-a914373942af')
    ->ipv4('68.183.121.157')
    ->registryEnabled(true)
    ->serviceSubnet('10.245.0.0/16')
    ->surgeUpgrade(true)
    ->tags(
        [
            'k8s',
            'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
            'production',
            'web-team'
        ]
    )
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
    ->vpcUuid('c33931f2-a26a-4e61-b85c-4e95a2ec431b')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



