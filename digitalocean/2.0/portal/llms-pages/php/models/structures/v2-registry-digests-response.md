# V2 Registry Digests Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRGlnZXN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegistryDigestsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `manifests` | [`?(LatestManifest[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/latest-manifest.md) | Optional | - | getManifests(): ?array | setManifests(?array manifests): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegistryDigestsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\LatestManifestBuilder;
use DigitalOceanApiLib\Models\Builders\BlobBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2RegistryDigestsResponse = V2RegistryDigestsResponseBuilder::init(
    MetaBuilder::init(
        3
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->manifests(
        [
            LatestManifestBuilder::init()
                ->blobs(
                    [
                        BlobBuilder::init()
                            ->compressedSizeBytes(1471)
                            ->digest('sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        BlobBuilder::init()
                            ->compressedSizeBytes(12)
                            ->digest('sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e')
                            ->additionalProperty('compressed_size_byte', ApiHelper::deserialize('2814446'))
                            ->build(),
                        BlobBuilder::init()
                            ->compressedSizeBytes(528)
                            ->digest('sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ]
                )
                ->compressedSizeBytes(1972332)
                ->digest('sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221')
                ->registryName('example')
                ->repository('repo-1')
                ->sizeBytes(2816445)
                ->tags(
                    [
                        'v1',
                        'v2'
                    ]
                )
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2021-04-09T23:54:25Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1')
                    ->next('https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1')
                    ->additionalProperty('first', ApiHelper::deserialize('"https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1"'))
                    ->additionalProperty('prev', ApiHelper::deserialize('"https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1"'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



