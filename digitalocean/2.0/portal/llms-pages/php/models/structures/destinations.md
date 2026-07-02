# Destinations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRlc3RpbmF0aW9ucw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Destinations`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `addresses` | `?(string[])` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. | getAddresses(): ?array | setAddresses(?array addresses): void |
| `dropletIds` | `?(int[])` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. | getDropletIds(): ?array | setDropletIds(?array dropletIds): void |
| `kubernetesIds` | `?(string[])` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. | getKubernetesIds(): ?array | setKubernetesIds(?array kubernetesIds): void |
| `loadBalancerUids` | `?(string[])` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. | getLoadBalancerUids(): ?array | setLoadBalancerUids(?array loadBalancerUids): void |
| `tags` | `?(string[])` | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DestinationsBuilder;
use DigitalOceanApiLib\ApiHelper;

$destinations = DestinationsBuilder::init()
    ->addresses(
        [
            '1.2.3.4',
            '18.0.0.0/8'
        ]
    )
    ->dropletIds(
        [
            8043964
        ]
    )
    ->kubernetesIds(
        [
            '41b74c5d-9bd0-5555-5555-a57c495b81a3'
        ]
    )
    ->loadBalancerUids(
        [
            '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ]
    )
    ->tags(
        [
            'tags7',
            'tags8',
            'tags9'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



