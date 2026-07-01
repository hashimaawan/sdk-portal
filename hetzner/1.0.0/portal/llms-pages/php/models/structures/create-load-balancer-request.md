# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Class Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `algorithm` | [`LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer | getAlgorithm(): LoadBalancerAlgorithm | setAlgorithm(LoadBalancerAlgorithm algorithm): void |
| `labels` | [`?Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels | setLabels(?Labels labels): void |
| `loadBalancerType` | `string` | Required | ID or name of the Load Balancer type this Load Balancer should be created with | getLoadBalancerType(): string | setLoadBalancerType(string loadBalancerType): void |
| `location` | `?string` | Optional | ID or name of Location to create Load Balancer in | getLocation(): ?string | setLocation(?string location): void |
| `name` | `string` | Required | Name of the Load Balancer | getName(): string | setName(string name): void |
| `network` | `?int` | Optional | ID of the network the Load Balancer should be attached to on creation | getNetwork(): ?int | setNetwork(?int network): void |
| `networkZone` | `?string` | Optional | Name of network zone | getNetworkZone(): ?string | setNetworkZone(?string networkZone): void |
| `publicInterface` | `?bool` | Optional | Enable or disable the public interface of the Load Balancer | getPublicInterface(): ?bool | setPublicInterface(?bool publicInterface): void |
| `services` | [`?(LoadBalancerService[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-service.md) | Optional | Array of services | getServices(): ?array | setServices(?array services): void |
| `targets` | [`?(LoadBalancerTarget[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-target.md) | Optional | Array of targets | getTargets(): ?array | setTargets(?array targets): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateLoadBalancerRequestBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerAlgorithmBuilder;
use HetznerCloudAPILib\Models\Type28Enum;
use HetznerCloudAPILib\Models\Builders\LabelsBuilder;

$createLoadBalancerRequest = CreateLoadBalancerRequestBuilder::init(
    LoadBalancerAlgorithmBuilder::init(
        Type28Enum::ROUND_ROBIN
    )->build(),
    'lb11',
    'Web Frontend'
)
    ->labels(
        LabelsBuilder::init()
            ->labelkey('labelkey4')
            ->build()
    )
    ->location('location2')
    ->network(123)
    ->networkZone('eu-central')
    ->publicInterface(true)
    ->build();
```



