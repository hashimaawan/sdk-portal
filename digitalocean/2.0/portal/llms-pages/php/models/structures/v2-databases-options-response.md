# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `options` | [`?Options`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/options.md) | Optional | - | getOptions(): ?Options | setOptions(?Options options): void |
| `versionAvailability` | [`?VersionAvailability`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/version-availability.md) | Optional | - | getVersionAvailability(): ?VersionAvailability | setVersionAvailability(?VersionAvailability versionAvailability): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesOptionsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\OptionsBuilder;
use DigitalOceanApiLib\Models\Builders\MongodbBuilder;
use DigitalOceanApiLib\Models\Builders\LayoutBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\MysqlBuilder;
use DigitalOceanApiLib\Models\Builders\PgBuilder;
use DigitalOceanApiLib\Models\Builders\RedisBuilder;
use DigitalOceanApiLib\Models\Builders\VersionAvailabilityBuilder;
use DigitalOceanApiLib\Models\Builders\Mongodb1Builder;

$v2DatabasesOptionsResponse = V2DatabasesOptionsResponseBuilder::init()
    ->options(
        OptionsBuilder::init()
            ->mongodb(
                MongodbBuilder::init()
                    ->regions(
                        [
                            'regions3',
                            'regions4'
                        ]
                    )
                    ->versions(
                        [
                            'versions3',
                            'versions4'
                        ]
                    )
                    ->layouts(
                        [
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->mysql(
                MysqlBuilder::init()
                    ->regions(
                        [
                            'regions9',
                            'regions0',
                            'regions1'
                        ]
                    )
                    ->versions(
                        [
                            'versions9',
                            'versions0',
                            'versions1'
                        ]
                    )
                    ->layouts(
                        [
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->pg(
                PgBuilder::init()
                    ->regions(
                        [
                            'regions3'
                        ]
                    )
                    ->versions(
                        [
                            'versions3'
                        ]
                    )
                    ->layouts(
                        [
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->redis(
                RedisBuilder::init()
                    ->regions(
                        [
                            'regions7'
                        ]
                    )
                    ->versions(
                        [
                            'versions7'
                        ]
                    )
                    ->layouts(
                        [
                            LayoutBuilder::init()
                                ->numNodes(190)
                                ->sizes(
                                    [
                                        'sizes2',
                                        'sizes3'
                                    ]
                                )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->versionAvailability(
        VersionAvailabilityBuilder::init()
            ->mongodb(
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
                        ->build(),
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
                        ->build()
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



