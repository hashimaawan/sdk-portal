# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJUDE


# Class Name

`PrimaryIP1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assigneeId` | `?int` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all | getAssigneeId(): ?int | setAssigneeId(?int assigneeId): void |
| `assigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` | getAssigneeType(): string | setAssigneeType(string assigneeType): void |
| `autoDelete` | `bool` | Required | Delete this Primary IP when the resource it is assigned to is deleted | getAutoDelete(): bool | setAutoDelete(bool autoDelete): void |
| `blocked` | `bool` | Required | Whether the IP is blocked | getBlocked(): bool | setBlocked(bool blocked): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at | getDatacenter(): Datacenter2 | setDatacenter(Datacenter2 datacenter): void |
| `dnsPtr` | [`DnsPtr[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries | getDnsPtr(): array | setDnsPtr(array dnsPtr): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `ip` | `string` | Required | IP address | getIp(): string | setIp(string ip): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/protection.md) | Required | Protection configuration for the Resource | getProtection(): Protection | setProtection(Protection protection): void |
| `type` | [`string(Type50Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-50.md) | Required | Type of the Primary IP | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PrimaryIP1Builder;
use HetznerCloudAPILib\Models\Builders\Datacenter2Builder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypesBuilder;
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Type50Enum;

$primaryIP1 = PrimaryIP1Builder::init(
    true,
    false,
    '2016-01-30T23:55:00+00:00',
    Datacenter2Builder::init(
        'Falkenstein DC Park 8',
        42,
        LocationBuilder::init(
            'Falkenstein',
            'DE',
            'Falkenstein DC Park 1',
            1,
            50.47612,
            12.370071,
            'fsn1',
            'eu-central'
        )->build(),
        'fsn1-dc8',
        ServerTypesBuilder::init(
            [
                1,
                2,
                3
            ],
            [
                1,
                2,
                3
            ],
            [
                1,
                2,
                3
            ]
        )->build()
    )->build(),
    [
        DnsPtrBuilder::init(
            'server.example.com',
            '2001:db8::1'
        )->build()
    ],
    42,
    '131.232.99.1',
    [
        'key0' => 'labels4',
        'key1' => 'labels3'
    ],
    'my-resource',
    ProtectionBuilder::init(
        false
    )->build(),
    Type50Enum::IPV4
)
    ->assigneeId(17)
    ->build();
```



