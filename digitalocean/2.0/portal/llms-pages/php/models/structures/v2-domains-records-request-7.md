# V2 Domains Records Request 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0Nw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DomainsRecordsRequest7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | `string` | Required | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. | getData(): string | setData(string data): void |
| `flags` | `?int` | Required | An unsigned integer between 0-255 used for CAA records. | getFlags(): ?int | setFlags(?int flags): void |
| `id` | `?int` | Optional, Read-only | A unique identifier for each domain record. | getId(): ?int | setId(?int id): void |
| `name` | `string` | Required | The host name, alias, or service being defined by the record. | getName(): string | setName(string name): void |
| `port` | `?int` | Required | The port for SRV records. | getPort(): ?int | setPort(?int port): void |
| `priority` | `?int` | Required | The priority for SRV and MX records. | getPriority(): ?int | setPriority(?int priority): void |
| `tag` | `?string` | Required | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" | getTag(): ?string | setTag(?string tag): void |
| `ttl` | `?int` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. | getTtl(): ?int | setTtl(?int ttl): void |
| `type` | `string` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... | getType(): string | setType(string type): void |
| `weight` | `?int` | Optional | The weight for SRV records. | getWeight(): ?int | setWeight(?int weight): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DomainsRecordsRequest7Builder;
use DigitalOceanApiLib\ApiHelper;

$v2DomainsRecordsRequest7 = V2DomainsRecordsRequest7Builder::init(
    'ns1.digitalocean.com',
    '@',
    'NS'
)
    ->flags(null)
    ->id(28448429)
    ->port(null)
    ->priority(null)
    ->tag(null)
    ->ttl(1800)
    ->weight(214)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



