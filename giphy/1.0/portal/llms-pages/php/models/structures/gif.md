# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRkdpZg


# Class Name

`Gif`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bitlyUrl` | `?string` | Optional | The unique bit.ly URL for this GIF | getBitlyUrl(): ?string | setBitlyUrl(?string bitlyUrl): void |
| `contentUrl` | `?string` | Optional | Currently unused | getContentUrl(): ?string | setContentUrl(?string contentUrl): void |
| `createDatetime` | `?DateTime` | Optional | The date this GIF was added to the GIPHY database. | getCreateDatetime(): ?\DateTime | setCreateDatetime(?\DateTime createDatetime): void |
| `embdedUrl` | `?string` | Optional | A URL used for embedding this GIF | getEmbdedUrl(): ?string | setEmbdedUrl(?string embdedUrl): void |
| `featuredTags` | `?(string[])` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) | getFeaturedTags(): ?array | setFeaturedTags(?array featuredTags): void |
| `id` | `?string` | Optional | This GIF's unique ID | getId(): ?string | setId(?string id): void |
| `images` | [`?Images`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. | getImages(): ?Images | setImages(?Images images): void |
| `importDatetime` | `?DateTime` | Optional | The creation or upload date from this GIF's source. | getImportDatetime(): ?\DateTime | setImportDatetime(?\DateTime importDatetime): void |
| `rating` | `?string` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R | getRating(): ?string | setRating(?string rating): void |
| `slug` | `?string` | Optional | The unique slug used in this GIF's URL | getSlug(): ?string | setSlug(?string slug): void |
| `source` | `?string` | Optional | The page on which this GIF was found | getSource(): ?string | setSource(?string source): void |
| `sourcePostUrl` | `?string` | Optional | The URL of the webpage on which this GIF was found. | getSourcePostUrl(): ?string | setSourcePostUrl(?string sourcePostUrl): void |
| `sourceTld` | `?string` | Optional | The top level domain of the source URL. | getSourceTld(): ?string | setSourceTld(?string sourceTld): void |
| `tags` | `?(string[])` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) | getTags(): ?array | setTags(?array tags): void |
| `trendingDatetime` | `?DateTime` | Optional | The date on which this gif was marked trending, if applicable. | getTrendingDatetime(): ?\DateTime | setTrendingDatetime(?\DateTime trendingDatetime): void |
| `type` | [`?string(TypeEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `TypeEnum::GIF` | getType(): ?string | setType(?string type): void |
| `updateDatetime` | `?DateTime` | Optional | The date on which this GIF was last updated. | getUpdateDatetime(): ?\DateTime | setUpdateDatetime(?\DateTime updateDatetime): void |
| `url` | `?string` | Optional | The unique URL for this GIF | getUrl(): ?string | setUrl(?string url): void |
| `user` | [`?User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. | getUser(): ?User | setUser(?User user): void |
| `username` | `?string` | Optional | The username this GIF is attached to, if applicable | getUsername(): ?string | setUsername(?string username): void |


# Example

```php
use GiphyAPILib\Models\Builders\GifBuilder;
use GiphyAPILib\Utils\DateTimeHelper;
use GiphyAPILib\Models\TypeEnum;

$gif = GifBuilder::init()
    ->bitlyUrl('http://gph.is/1gsWDcL')
    ->contentUrl('content_url4')
    ->createDatetime(DateTimeHelper::fromRfc3339DateTime('2013-08-01 12:41:48'))
    ->embdedUrl('http://giphy.com/embed/YsTs5ltWtEhnq')
    ->featuredTags(
        [
            'featured_tags0'
        ]
    )
    ->id('YsTs5ltWtEhnq')
    ->importDatetime(DateTimeHelper::fromRfc3339DateTime('2013-08-01 12:41:48'))
    ->rating('g')
    ->slug('confused-flying-YsTs5ltWtEhnq')
    ->source('http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/')
    ->sourcePostUrl('http://cheezburger.com/5282328320')
    ->sourceTld('cheezburger.com')
    ->trendingDatetime(DateTimeHelper::fromRfc3339DateTime('2013-08-01 12:41:48'))
    ->type(TypeEnum::GIF)
    ->updateDatetime(DateTimeHelper::fromRfc3339DateTime('2013-08-01 12:41:48'))
    ->url('http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq')
    ->username('JoeCool4000')
    ->build();
```



