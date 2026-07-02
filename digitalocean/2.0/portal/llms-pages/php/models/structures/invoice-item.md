# Invoice Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkludm9pY2VJdGVt

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`InvoiceItem`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `?string` | Optional | Billed amount of this invoice item. Billed in USD. | getAmount(): ?string | setAmount(?string amount): void |
| `description` | `?string` | Optional | Description of the invoice item. | getDescription(): ?string | setDescription(?string description): void |
| `duration` | `?string` | Optional | Duration of time this invoice item was used and subsequently billed. | getDuration(): ?string | setDuration(?string duration): void |
| `durationUnit` | `?string` | Optional | Unit of time for duration. | getDurationUnit(): ?string | setDurationUnit(?string durationUnit): void |
| `endTime` | `?string` | Optional | Time the invoice item stopped being billed for usage. | getEndTime(): ?string | setEndTime(?string endTime): void |
| `groupDescription` | `?string` | Optional | Description of the invoice item when it is a grouped set of usage, such  as DOKS or databases. | getGroupDescription(): ?string | setGroupDescription(?string groupDescription): void |
| `product` | `?string` | Optional | Name of the product being billed in the invoice item. | getProduct(): ?string | setProduct(?string product): void |
| `projectName` | `?string` | Optional | Name of the DigitalOcean Project this resource belongs to. | getProjectName(): ?string | setProjectName(?string projectName): void |
| `resourceId` | `?string` | Optional | ID of the resource billing in the invoice item if available. | getResourceId(): ?string | setResourceId(?string resourceId): void |
| `resourceUuid` | `?string` | Optional | UUID of the resource billing in the invoice item if available. | getResourceUuid(): ?string | setResourceUuid(?string resourceUuid): void |
| `startTime` | `?string` | Optional | Time the invoice item began to be billed for usage. | getStartTime(): ?string | setStartTime(?string startTime): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\InvoiceItemBuilder;
use DigitalOceanApiLib\ApiHelper;

$invoiceItem = InvoiceItemBuilder::init()
    ->amount('12.34')
    ->description('a56e086a317d8410c8b4cfd1f4dc9f82')
    ->duration('744')
    ->durationUnit('Hours')
    ->endTime('2020-02-01T00:00:00Z')
    ->groupDescription('my-doks-cluster')
    ->product('Kubernetes Clusters')
    ->projectName('web')
    ->resourceId('2353624')
    ->resourceUuid('711157cb-37c8-4817-b371-44fa3504a39c')
    ->startTime('2020-01-01T00:00:00Z')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



