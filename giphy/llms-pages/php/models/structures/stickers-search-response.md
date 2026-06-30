# Stickers Search Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/php/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBTZWFyY2glMjUyMFJlc3BvbnNl


# Class Name

`StickersSearchResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(Gif[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/php/models/structures/gif.md) | Optional | - | getData(): ?array | setData(?array data): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/php/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `pagination` | [`?Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/php/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. | getPagination(): ?Pagination | setPagination(?Pagination pagination): void |


# Example

```php
use GiphyAPILib\Models\Builders\StickersSearchResponseBuilder;
use GiphyAPILib\Models\Builders\GifBuilder;
use GiphyAPILib\Utils\DateTimeHelper;
use GiphyAPILib\Models\Builders\MetaBuilder;
use GiphyAPILib\Models\Builders\PaginationBuilder;

$stickersSearchResponse = StickersSearchResponseBuilder::init()
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
                ->build()
        ]
    )
    ->meta(
        MetaBuilder::init()
            ->msg('msg8')
            ->responseId('response_id0')
            ->status(98)
            ->build()
    )
    ->pagination(
        PaginationBuilder::init()
            ->count(192)
            ->offset(240)
            ->totalCount(100)
            ->build()
    )
    ->build();
```



