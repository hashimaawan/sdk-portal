# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type array.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `boundTo` | `?int` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. | getBoundTo(): ?int | setBoundTo(?int boundTo): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `createdFrom` | [`?CreatedFrom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/created-from.md) | Required | Information about the Server the Image was created from | getCreatedFrom(): ?CreatedFrom | setCreatedFrom(?CreatedFrom createdFrom): void |
| `deleted` | `?string` | Required | Point in time where the Image was deleted (in ISO-8601 format) | getDeleted(): ?string | setDeleted(?string deleted): void |
| `deprecated` | `?string` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) | getDeprecated(): ?string | setDeprecated(?string deprecated): void |
| `description` | `string` | Required | Description of the Image | getDescription(): string | setDescription(string description): void |
| `diskSize` | `float` | Required | Size of the disk contained in the Image in GB | getDiskSize(): float | setDiskSize(float diskSize): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `imageSize` | `?float` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. | getImageSize(): ?float | setImageSize(?float imageSize): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `?string` | Required | Unique identifier of the Image. This value is only set for system Images. | getName(): ?string | setName(?string name): void |
| `osFlavor` | [`string(OsFlavor)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image | getOsFlavor(): string | setOsFlavor(string osFlavor): void |
| `osVersion` | `?string` | Required | Operating system version | getOsVersion(): ?string | setOsVersion(?string osVersion): void |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection.md) | Required | Protection configuration for the Resource | getProtection(): Protection | setProtection(Protection protection): void |
| `rapidDeploy` | `?bool` | Optional | Indicates that rapid deploy of the Image is available | getRapidDeploy(): ?bool | setRapidDeploy(?bool rapidDeploy): void |
| `status` | [`string(Status24)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable | getStatus(): string | setStatus(string status): void |
| `type` | [`string(Type22)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-22.md) | Required | Type of the Image | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ImageBuilder;
use HetznerCloudApiLib\Models\OsFlavor;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status24;
use HetznerCloudApiLib\Models\Type22;
use HetznerCloudApiLib\Models\Builders\CreatedFromBuilder;

$image = ImageBuilder::init(
    '2016-01-30T23:55:00+00:00',
    'Ubuntu 20.04 Standard 64 bit',
    10,
    42,
    [
        'key0' => 'labels4'
    ],
    OsFlavor::UBUNTU,
    ProtectionBuilder::init(
        false
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    Status24::UNAVAILABLE,
    Type22::SNAPSHOT
)
    ->boundTo(null)
    ->createdFrom(
        CreatedFromBuilder::init(
            1,
            'Server'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->deleted(null)
    ->deprecated('2018-02-28T00:00:00+00:00')
    ->imageSize(2.3)
    ->name('ubuntu-20.04')
    ->osVersion('20.04')
    ->rapidDeploy(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



