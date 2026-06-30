# Playlist Track Object Track

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tPYmplY3RUcmFjaw


# Class Name

`PlaylistTrackObjectTrack`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/track-object.md) | PlaylistTrackObjectTrack.FromTrackObject(TrackObject trackObject) |
| [`EpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/episode-object.md) | PlaylistTrackObjectTrack.FromEpisodeObject(EpisodeObject episodeObject) |


# TrackObject

## Initialization Code

### Example

```csharp
PlaylistTrackObjectTrack value = PlaylistTrackObjectTrack.FromTrackObject(
    new TrackObject
    {
    }
);
```


# EpisodeObject

## Initialization Code

### Example

```csharp
PlaylistTrackObjectTrack value = PlaylistTrackObjectTrack.FromEpisodeObject(
    new EpisodeObject
    {
        AudioPreviewUrl = "https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17",
        Description = "A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n",
        HtmlDescription = "<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n",
        DurationMs = 1686230,
        MExplicit = false,
        ExternalUrls = new ExternalUrlObject
        {
        },
        Href = "https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ",
        Id = "5Xt5DXGzch68nYYamXrNxZ",
        Images = new List<ImageObject>
        {
            new ImageObject
            {
                Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                Height = 300,
                Width = 300,
            },
        },
        IsExternallyHosted = false,
        IsPlayable = false,
        Languages = new List<string>
        {
            "fr",
            "en",
        },
        Name = "Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n",
        ReleaseDate = "1981-12-15",
        ReleaseDatePrecision = ReleaseDatePrecision.Day,
        Type = "episode",
        Uri = "spotify:episode:0zLhl3WsOCQHbe1BPTiHgr",
        Show = new ShowBase
        {
            AvailableMarkets = new List<string>
            {
                "available_markets0",
                "available_markets1",
                "available_markets2",
            },
            Copyrights = new List<CopyrightObject>
            {
                new CopyrightObject
                {
                },
            },
            Description = "description4",
            HtmlDescription = "html_description4",
            MExplicit = false,
            ExternalUrls = new ExternalUrlObject
            {
            },
            Href = "href8",
            Id = "id6",
            Images = new List<ImageObject>
            {
                new ImageObject
                {
                    Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                    Height = 300,
                    Width = 300,
                },
            },
            IsExternallyHosted = false,
            Languages = new List<string>
            {
                "languages7",
                "languages6",
                "languages5",
            },
            MediaType = "media_type6",
            Name = "name6",
            Publisher = "publisher6",
            Type = "show",
            Uri = "uri0",
            TotalEpisodes = 198,
        },
        Language = "en",
    }
);
```



