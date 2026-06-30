# Currently Playing Context Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type array.*


# Class Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `device` | [`?DeviceObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/device-object.md) | Optional | The device that is currently active. | getDevice(): ?DeviceObject | setDevice(?DeviceObject device): void |
| `repeatState` | `?string` | Optional | off, track, context | getRepeatState(): ?string | setRepeatState(?string repeatState): void |
| `shuffleState` | `?bool` | Optional | If shuffle is on or off. | getShuffleState(): ?bool | setShuffleState(?bool shuffleState): void |
| `context` | [`?ContextObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. | getContext(): ?ContextObject | setContext(?ContextObject context): void |
| `timestamp` | `?int` | Optional | Unix Millisecond Timestamp when data was fetched. | getTimestamp(): ?int | setTimestamp(?int timestamp): void |
| `progressMs` | `?int` | Optional | Progress into the currently playing track or episode. Can be `null`. | getProgressMs(): ?int | setProgressMs(?int progressMs): void |
| `isPlaying` | `?bool` | Optional | If something is currently playing, return `true`. | getIsPlaying(): ?bool | setIsPlaying(?bool isPlaying): void |
| `item` | [TrackObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/track-object.md)\|[EpisodeObject](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/episode-object.md)\|null | Optional | This is a container for one-of cases. | getItem(): | setItem( item): void |
| `currentlyPlayingType` | `?string` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. | getCurrentlyPlayingType(): ?string | setCurrentlyPlayingType(?string currentlyPlayingType): void |
| `actions` | [`?DisallowsObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. | getActions(): ?DisallowsObject | setActions(?DisallowsObject actions): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CurrentlyPlayingContextObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\DeviceObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ContextObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;

$currentlyPlayingContextObject = CurrentlyPlayingContextObjectBuilder::init()
    ->device(
        DeviceObjectBuilder::init()
            ->id('id6')
            ->isActive(false)
            ->isPrivateSession(false)
            ->isRestricted(false)
            ->name('name6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->repeatState('repeat_state8')
    ->shuffleState(false)
    ->context(
        ContextObjectBuilder::init()
            ->type('type8')
            ->href('href4')
            ->externalUrls(
                ExternalUrlObjectBuilder::init()
                    ->spotify('spotify6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->uri('uri6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->timestamp(48)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



