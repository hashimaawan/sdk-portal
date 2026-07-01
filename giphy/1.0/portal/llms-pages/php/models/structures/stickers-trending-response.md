# Stickers Trending Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBUcmVuZGluZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`StickersTrendingResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(Gif[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/gif.md) | Optional | - | getData(): ?array | setData(?array data): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `pagination` | [`?Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. | getPagination(): ?Pagination | setPagination(?Pagination pagination): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use GiphyApiLib\Models\Builders\StickersTrendingResponseBuilder;
use GiphyApiLib\Models\Builders\GifBuilder;
use GiphyApiLib\Utils\DateTimeHelper;
use GiphyApiLib\ApiHelper;
use GiphyApiLib\Models\Builders\MetaBuilder;
use GiphyApiLib\Models\Builders\PaginationBuilder;

$stickersTrendingResponse = StickersTrendingResponseBuilder::init()
    ->data(
        [
            GifBuilder::init()
                ->bitlyUrl('bitly_url0')
                ->contentUrl('content_url4')
                ->createDatetime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->embdedUrl('embded_url8')
                ->featuredTags(
                    [
                        'featured_tags0'
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->meta(
        MetaBuilder::init()
            ->msg('msg8')
            ->responseId('response_id0')
            ->status(98)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->pagination(
        PaginationBuilder::init()
            ->count(192)
            ->offset(240)
            ->totalCount(100)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



