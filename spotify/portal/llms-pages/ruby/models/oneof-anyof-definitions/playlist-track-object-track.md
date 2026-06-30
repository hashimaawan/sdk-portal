# Playlist Track Object Track

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tPYmplY3RUcmFjaw


# Data Type

`TrackObject | EpisodeObject`


# Cases

| Type |
|  --- |
| [`TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/track-object.md) |
| [`EpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/episode-object.md) |


# TrackObject

## Initialization Code

### Example

```ruby
value = TrackObject.new
```


# EpisodeObject

## Initialization Code

### Example

```ruby
value = EpisodeObject.new(
  audio_preview_url: 'https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
  description: 'A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n',
  html_description: '<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n',
  duration_ms: 1686230,
  explicit: false,
  external_urls: ExternalUrlObject.new,
  href: 'https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ',
  id: '5Xt5DXGzch68nYYamXrNxZ',
  images: [
    ImageObject.new(
      url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
      height: 300,
      width: 300
    )
  ],
  is_externally_hosted: false,
  is_playable: false,
  languages: [
    'fr',
    'en'
  ],
  name: 'Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n',
  release_date: '1981-12-15',
  release_date_precision: ReleaseDatePrecision::DAY,
  type: 'episode',
  uri: 'spotify:episode:0zLhl3WsOCQHbe1BPTiHgr',
  show: ShowBase.new(
    available_markets: [
      'available_markets0',
      'available_markets1',
      'available_markets2'
    ],
    copyrights: [
      CopyrightObject.new
    ],
    description: 'description4',
    html_description: 'html_description4',
    explicit: false,
    external_urls: ExternalUrlObject.new,
    href: 'href8',
    id: 'id6',
    images: [
      ImageObject.new(
        url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
        height: 300,
        width: 300
      )
    ],
    is_externally_hosted: false,
    languages: [
      'languages7',
      'languages6',
      'languages5'
    ],
    media_type: 'media_type6',
    name: 'name6',
    publisher: 'publisher6',
    type: 'show',
    uri: 'uri0',
    total_episodes: 198
  ),
  language: 'en'
)
```



