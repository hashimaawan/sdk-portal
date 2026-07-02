# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `dropletIds` | `?(int[])` | Optional | An array containing the IDs of the Droplets assigned to the firewall. | getDropletIds(): ?array | setDropletIds(?array dropletIds): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` | getName(): ?string | setName(?string name): void |
| `pendingChanges` | [`?(PendingChange[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. | getPendingChanges(): ?array | setPendingChanges(?array pendingChanges): void |
| `status` | [`?string(Status9)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". | getStatus(): ?string | setStatus(?string status): void |
| `tags` | `?(string[])` | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `inboundRules` | [`?(InboundRule[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/inbound-rule.md) | Optional | - | getInboundRules(): ?array | setInboundRules(?array inboundRules): void |
| `outboundRules` | [`?(OutboundRule[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/outbound-rule.md) | Optional | - | getOutboundRules(): ?array | setOutboundRules(?array outboundRules): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\FirewallBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\PendingChangeBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status9;

$firewall = FirewallBuilder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-05-23T21:24:00Z'))
    ->dropletIds(
        [
            8043964
        ]
    )
    ->id('bb4b2611-3d72-467b-8602-280330ecd65c')
    ->name('firewall')
    ->pendingChanges(
        [
            PendingChangeBuilder::init()
                ->dropletId(8043964)
                ->removing(false)
                ->status('waiting')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->status(Status9::WAITING)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



