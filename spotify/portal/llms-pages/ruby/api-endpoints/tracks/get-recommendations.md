# Get-Recommendations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```ruby
def get_recommendations(limit: 20,
                        market: nil,
                        seed_artists: nil,
                        seed_genres: nil,
                        seed_tracks: nil,
                        min_acousticness: nil,
                        max_acousticness: nil,
                        target_acousticness: nil,
                        min_danceability: nil,
                        max_danceability: nil,
                        target_danceability: nil,
                        min_duration_ms: nil,
                        max_duration_ms: nil,
                        target_duration_ms: nil,
                        min_energy: nil,
                        max_energy: nil,
                        target_energy: nil,
                        min_instrumentalness: nil,
                        max_instrumentalness: nil,
                        target_instrumentalness: nil,
                        min_key: nil,
                        max_key: nil,
                        target_key: nil,
                        min_liveness: nil,
                        max_liveness: nil,
                        target_liveness: nil,
                        min_loudness: nil,
                        max_loudness: nil,
                        target_loudness: nil,
                        min_mode: nil,
                        max_mode: nil,
                        target_mode: nil,
                        min_popularity: nil,
                        max_popularity: nil,
                        target_popularity: nil,
                        min_speechiness: nil,
                        max_speechiness: nil,
                        target_speechiness: nil,
                        min_tempo: nil,
                        max_tempo: nil,
                        target_tempo: nil,
                        min_time_signature: nil,
                        max_time_signature: nil,
                        target_time_signature: nil,
                        min_valence: nil,
                        max_valence: nil,
                        target_valence: nil)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `Integer` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `String` | Query, Optional | - |
| `seed_artists` | `String` | Query, Optional | - |
| `seed_genres` | `String` | Query, Optional | - |
| `seed_tracks` | `String` | Query, Optional | - |
| `min_acousticness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_acousticness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_acousticness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_danceability` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_danceability` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_danceability` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_duration_ms` | `Integer` | Query, Optional | - |
| `max_duration_ms` | `Integer` | Query, Optional | - |
| `target_duration_ms` | `Integer` | Query, Optional | - |
| `min_energy` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_energy` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_energy` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_instrumentalness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_instrumentalness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_instrumentalness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_key` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `max_key` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `target_key` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `min_liveness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_liveness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_liveness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_loudness` | `Float` | Query, Optional | - |
| `max_loudness` | `Float` | Query, Optional | - |
| `target_loudness` | `Float` | Query, Optional | - |
| `min_mode` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_mode` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_mode` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_popularity` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `max_popularity` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `target_popularity` | `Integer` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `min_speechiness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_speechiness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_speechiness` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_tempo` | `Float` | Query, Optional | - |
| `max_tempo` | `Float` | Query, Optional | - |
| `target_tempo` | `Float` | Query, Optional | - |
| `min_time_signature` | `Integer` | Query, Optional | **Constraints**: `<= 11` |
| `max_time_signature` | `Integer` | Query, Optional | - |
| `target_time_signature` | `Integer` | Query, Optional | - |
| `min_valence` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_valence` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_valence` | `Float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`RecommendationsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/recommendations-object.md).


# Example Usage

```ruby
limit = 10

market = 'ES'

seed_artists = '4NHQUGzhtTLFvgF5SZesLK'

seed_genres = 'classical,country'

seed_tracks = '0c6xIDDpzE81m2q797ordA'

result = tracks_api.get_recommendations(
  limit: limit,
  market: market,
  seed_artists: seed_artists,
  seed_genres: seed_genres,
  seed_tracks: seed_tracks
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/exceptions/too-many-requests.md) |



