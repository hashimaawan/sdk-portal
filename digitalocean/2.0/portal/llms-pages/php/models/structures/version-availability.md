# Version Availability

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlZlcnNpb25BdmFpbGFiaWxpdHk

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`VersionAvailability`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `mongodb` | [`?(Mongodb1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | getMongodb(): ?array | setMongodb(?array mongodb): void |
| `mysql` | [`?(Mongodb1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | getMysql(): ?array | setMysql(?array mysql): void |
| `pg` | [`?(Mongodb1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | getPg(): ?array | setPg(?array pg): void |
| `redis` | [`?(Mongodb1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines | getRedis(): ?array | setRedis(?array redis): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\VersionAvailabilityBuilder;
use DigitalOceanApiLib\Models\Builders\Mongodb1Builder;
use DigitalOceanApiLib\ApiHelper;

$versionAvailability = VersionAvailabilityBuilder::init()
    ->mongodb(
        [
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability4')
                ->endOfLife('end_of_life4')
                ->version('version4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->mysql(
        [
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability0')
                ->endOfLife('end_of_life0')
                ->version('version0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->pg(
        [
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability4')
                ->endOfLife('end_of_life4')
                ->version('version4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability4')
                ->endOfLife('end_of_life4')
                ->version('version4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability4')
                ->endOfLife('end_of_life4')
                ->version('version4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->redis(
        [
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability8')
                ->endOfLife('end_of_life8')
                ->version('version8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Mongodb1Builder::init()
                ->endOfAvailability('end_of_availability8')
                ->endOfLife('end_of_life8')
                ->version('version8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



