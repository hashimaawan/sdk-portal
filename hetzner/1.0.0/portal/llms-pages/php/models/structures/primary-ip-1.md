# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJUDE

*This model accepts additional fields of type array.*


# Class Name

`PrimaryIp1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assigneeId` | `?int` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all | getAssigneeId(): ?int | setAssigneeId(?int assigneeId): void |
| `assigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` | getAssigneeType(): string | setAssigneeType(string assigneeType): void |
| `autoDelete` | `bool` | Required | Delete this Primary IP when the resource it is assigned to is deleted | getAutoDelete(): bool | setAutoDelete(bool autoDelete): void |
| `blocked` | `bool` | Required | Whether the IP is blocked | getBlocked(): bool | setBlocked(bool blocked): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at | getDatacenter(): Datacenter2 | setDatacenter(Datacenter2 datacenter): void |
| `dnsPtr` | [`DnsPtr[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries | getDnsPtr(): array | setDnsPtr(array dnsPtr): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `ip` | `string` | Required | IP address | getIp(): string | setIp(string ip): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection.md) | Required | Protection configuration for the Resource | getProtection(): Protection | setProtection(Protection protection): void |
| `type` | [`string(Type50)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-50.md) | Required | Type of the Primary IP | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PrimaryIp1Builder;
use HetznerCloudApiLib\Models\Builders\Datacenter2Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;
use HetznerCloudApiLib\Models\Builders\DnsPtrBuilder;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Type50;

$primaryIp1 = PrimaryIp1Builder::init(
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
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
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
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        DnsPtrBuilder::init(
            'server.example.com',
            '2001:db8::1'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    42,
    '131.232.99.1',
    [
        'key0' => 'labels0'
    ],
    'my-resource',
    ProtectionBuilder::init(
        false
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    Type50::IPV4
)
    ->assigneeId(17)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



