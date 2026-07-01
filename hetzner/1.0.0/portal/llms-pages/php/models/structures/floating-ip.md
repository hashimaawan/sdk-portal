# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

*This model accepts additional fields of type array.*


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `blocked` | `bool` | Required | Whether the IP is blocked | getBlocked(): bool | setBlocked(bool blocked): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `description` | `?string` | Required | Description of the Resource | getDescription(): ?string | setDescription(?string description): void |
| `dnsPtr` | [`DnsPtr[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries | getDnsPtr(): array | setDnsPtr(array dnsPtr): void |
| `homeLocation` | [`HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. | getHomeLocation(): HomeLocation | setHomeLocation(HomeLocation homeLocation): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `ip` | `string` | Required | IP address | getIp(): string | setIp(string ip): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection.md) | Required | Protection configuration for the Resource | getProtection(): Protection | setProtection(Protection protection): void |
| `server` | `?int` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all | getServer(): ?int | setServer(?int server): void |
| `type` | [`string(Type16)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-16.md) | Required | Type of the Floating IP | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FloatingIpBuilder;
use HetznerCloudApiLib\Models\Builders\DnsPtrBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\HomeLocationBuilder;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Type16;

$floatingIp = FloatingIpBuilder::init(
    false,
    '2016-01-30T23:55:00+00:00',
    [
        DnsPtrBuilder::init(
            'server.example.com',
            '2001:db8::1'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    HomeLocationBuilder::init(
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
    42,
    '131.232.99.1',
    [
        'key0' => 'labels6'
    ],
    'my-resource',
    ProtectionBuilder::init(
        false
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    Type16::IPV4
)
    ->description('this describes my resource')
    ->server(42)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



