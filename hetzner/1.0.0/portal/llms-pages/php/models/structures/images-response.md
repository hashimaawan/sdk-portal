# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `images` | [`Image[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image.md) | Required | - | getImages(): array | setImages(array images): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ImagesResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ImageBuilder;
use HetznerCloudApiLib\Models\OsFlavor;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status24;
use HetznerCloudApiLib\Models\Type22;
use HetznerCloudApiLib\Models\Builders\CreatedFromBuilder;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

$imagesResponse = ImagesResponseBuilder::init(
    [
        ImageBuilder::init(
            '2016-01-30T23:55:00+00:00',
            'Ubuntu 20.04 Standard 64 bit',
            10,
            42,
            [
                'key0' => 'labels0',
                'key1' => 'labels1'
            ],
            OsFlavor::UBUNTU,
            ProtectionBuilder::init(
                false
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Status24::AVAILABLE,
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
            ->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



