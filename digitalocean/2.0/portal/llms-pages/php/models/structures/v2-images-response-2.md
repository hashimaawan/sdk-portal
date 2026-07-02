# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/image-1.md) | Required | - | getImage(): Image1 | setImage(Image1 image): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ImagesResponse2Builder;
use DigitalOceanApiLib\Models\Builders\Image1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Distribution;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\Models\Status7;
use DigitalOceanApiLib\Models\Type9;
use DigitalOceanApiLib\ApiHelper;

$v2ImagesResponse2 = V2ImagesResponse2Builder::init(
    Image1Builder::init()
        ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-05-04T22:23:02Z'))
        ->description('description6')
        ->distribution(Distribution::UBUNTU)
        ->errorMessage('error_message8')
        ->id(7555620)
        ->minDiskSize(20)
        ->name('Nifty New Snapshot')
        ->public(true)
        ->regions(
            [
                Region2::NYC1,
                Region2::NYC2
            ]
        )
        ->sizeGigabytes(2.34)
        ->slug('nifty1')
        ->status(Status7::NEW_)
        ->tags(
            [
                'base-image',
                'prod'
            ]
        )
        ->type(Type9::SNAPSHOT)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



