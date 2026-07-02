# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Options`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `mongodb` | [`?Mongodb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mongodb.md) | Optional | - | getMongodb(): ?Mongodb | setMongodb(?Mongodb mongodb): void |
| `mysql` | [`?Mysql`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mysql.md) | Optional | - | getMysql(): ?Mysql | setMysql(?Mysql mysql): void |
| `pg` | [`?Pg`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pg.md) | Optional | - | getPg(): ?Pg | setPg(?Pg pg): void |
| `redis` | [`?Redis`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/redis.md) | Optional | - | getRedis(): ?Redis | setRedis(?Redis redis): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\OptionsBuilder;
use DigitalOceanApiLib\Models\Builders\MongodbBuilder;
use DigitalOceanApiLib\Models\Builders\LayoutBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\MysqlBuilder;
use DigitalOceanApiLib\Models\Builders\PgBuilder;
use DigitalOceanApiLib\Models\Builders\RedisBuilder;

$options = OptionsBuilder::init()
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
    ->build();
```



