# Stickers Random Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBSYW5kb20lMjUyMFJlc3BvbnNl


# Class Name

`StickersRandomResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/gif.md) | Optional | - | getData(): ?Gif | setData(?Gif data): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use GiphyAPILib\Models\Builders\StickersRandomResponseBuilder;
use GiphyAPILib\Models\Builders\GifBuilder;
use GiphyAPILib\Utils\DateTimeHelper;
use GiphyAPILib\Models\Builders\MetaBuilder;

$stickersRandomResponse = StickersRandomResponseBuilder::init()
    ->data(
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
    )
    ->meta(
        MetaBuilder::init()
            ->msg('msg8')
            ->responseId('response_id0')
            ->status(98)
            ->build()
    )
    ->build();
```



