# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `automount` | `?bool` | Optional | Auto-mount Volumes after attach | getAutomount(): ?bool | setAutomount(?bool automount): void |
| `datacenter` | `?string` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) | getDatacenter(): ?string | setDatacenter(?string datacenter): void |
| `firewalls` | [`?(Firewall4[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time | getFirewalls(): ?array | setFirewalls(?array firewalls): void |
| `image` | `string` | Required | ID or name of the Image the Server is created from | getImage(): string | setImage(string image): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `location` | `?string` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) | getLocation(): ?string | setLocation(?string location): void |
| `name` | `string` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) | getName(): string | setName(string name): void |
| `networks` | `?(int[])` | Optional | Network IDs which should be attached to the Server private network interface at the creation time | getNetworks(): ?array | setNetworks(?array networks): void |
| `placementGroup` | `?int` | Optional | ID of the Placement Group the server should be in | getPlacementGroup(): ?int | setPlacementGroup(?int placementGroup): void |
| `publicNet` | [`?PublicNet5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/public-net-5.md) | Optional | Public Network options | getPublicNet(): ?PublicNet5 | setPublicNet(?PublicNet5 publicNet): void |
| `serverType` | `string` | Required | ID or name of the Server type this Server should be created with | getServerType(): string | setServerType(string serverType): void |
| `sshKeys` | `?(string[])` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time | getSshKeys(): ?array | setSshKeys(?array sshKeys): void |
| `startAfterCreate` | `?bool` | Optional | Start Server right after creation. Defaults to true. | getStartAfterCreate(): ?bool | setStartAfterCreate(?bool startAfterCreate): void |
| `userData` | `?string` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. | getUserData(): ?string | setUserData(?string userData): void |
| `volumes` | `?(int[])` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateServerRequestBuilder;
use HetznerCloudApiLib\Models\Builders\Firewall4Builder;
use HetznerCloudApiLib\ApiHelper;

$createServerRequest = CreateServerRequestBuilder::init(
    'ubuntu-20.04',
    'my-server',
    'cx11'
)
    ->automount(false)
    ->datacenter('nbg1-dc3')
    ->firewalls(
        [
            Firewall4Builder::init()
                ->firewall(38)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->location('nbg1')
    ->networks(
        [
            456
        ]
    )
    ->placementGroup(1)
    ->sshKeys(
        [
            'my-ssh-key'
        ]
    )
    ->startAfterCreate(true)
    ->userData('#cloud-config
runcmd:
- [touch, /root/cloud-init-worked]
')
    ->volumes(
        [
            123
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



