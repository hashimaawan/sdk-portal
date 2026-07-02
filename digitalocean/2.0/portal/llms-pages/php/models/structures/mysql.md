# Mysql

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk15c3Fs

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Mysql`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `regions` | `?(string[])` | Optional, Read-only | An array of strings containing the names of available regions | getRegions(): ?array | setRegions(?array regions): void |
| `versions` | `?(string[])` | Optional, Read-only | An array of strings containing the names of available regions | getVersions(): ?array | setVersions(?array versions): void |
| `layouts` | [`?(Layout[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). | getLayouts(): ?array | setLayouts(?array layouts): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MysqlBuilder;
use DigitalOceanApiLib\Models\Builders\LayoutBuilder;
use DigitalOceanApiLib\ApiHelper;

$mysql = MysqlBuilder::init()
    ->regions(
        [
            'ams3',
            'blr1'
        ]
    )
    ->versions(
        [
            '4.4',
            '5.0'
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
    ->build();
```



