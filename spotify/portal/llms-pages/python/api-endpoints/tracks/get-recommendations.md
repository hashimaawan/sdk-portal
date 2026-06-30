# Get-Recommendations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0ZSUyRlRyYWNrcyUyRmdldC1yZWNvbW1lbmRhdGlvbnM

Recommendations are generated based on the available information for a given seed entity and matched against similar artists and tracks. If there is sufficient information about the provided seeds, a list of tracks will be returned together with pool size details.

For artists and tracks that are very new or obscure there might not be enough data to generate a list of tracks.

```python
def get_recommendations(self,
                       limit=20,
                       market=None,
                       seed_artists=None,
                       seed_genres=None,
                       seed_tracks=None,
                       min_acousticness=None,
                       max_acousticness=None,
                       target_acousticness=None,
                       min_danceability=None,
                       max_danceability=None,
                       target_danceability=None,
                       min_duration_ms=None,
                       max_duration_ms=None,
                       target_duration_ms=None,
                       min_energy=None,
                       max_energy=None,
                       target_energy=None,
                       min_instrumentalness=None,
                       max_instrumentalness=None,
                       target_instrumentalness=None,
                       min_key=None,
                       max_key=None,
                       target_key=None,
                       min_liveness=None,
                       max_liveness=None,
                       target_liveness=None,
                       min_loudness=None,
                       max_loudness=None,
                       target_loudness=None,
                       min_mode=None,
                       max_mode=None,
                       target_mode=None,
                       min_popularity=None,
                       max_popularity=None,
                       target_popularity=None,
                       min_speechiness=None,
                       max_speechiness=None,
                       target_speechiness=None,
                       min_tempo=None,
                       max_tempo=None,
                       target_tempo=None,
                       min_time_signature=None,
                       max_time_signature=None,
                       target_time_signature=None,
                       min_valence=None,
                       max_valence=None,
                       target_valence=None)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `market` | `str` | Query, Optional | - |
| `seed_artists` | `str` | Query, Optional | - |
| `seed_genres` | `str` | Query, Optional | - |
| `seed_tracks` | `str` | Query, Optional | - |
| `min_acousticness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_acousticness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_acousticness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_danceability` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_danceability` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_danceability` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_duration_ms` | `int` | Query, Optional | - |
| `max_duration_ms` | `int` | Query, Optional | - |
| `target_duration_ms` | `int` | Query, Optional | - |
| `min_energy` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_energy` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_energy` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_instrumentalness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_instrumentalness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_instrumentalness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_key` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `max_key` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `target_key` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 11` |
| `min_liveness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_liveness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_liveness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_loudness` | `float` | Query, Optional | - |
| `max_loudness` | `float` | Query, Optional | - |
| `target_loudness` | `float` | Query, Optional | - |
| `min_mode` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_mode` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_mode` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_popularity` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `max_popularity` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `target_popularity` | `int` | Query, Optional | **Constraints**: `>= 0`, `<= 100` |
| `min_speechiness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_speechiness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_speechiness` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `min_tempo` | `float` | Query, Optional | - |
| `max_tempo` | `float` | Query, Optional | - |
| `target_tempo` | `float` | Query, Optional | - |
| `min_time_signature` | `int` | Query, Optional | **Constraints**: `<= 11` |
| `max_time_signature` | `int` | Query, Optional | - |
| `target_time_signature` | `int` | Query, Optional | - |
| `min_valence` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `max_valence` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |
| `target_valence` | `float` | Query, Optional | **Constraints**: `>= 0`, `<= 1` |


# Response Type

**200**: A set of recommendations

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`RecommendationsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/recommendations-object.md).


# Example Usage

```python
limit = 10

market = 'ES'

seed_artists = '4NHQUGzhtTLFvgF5SZesLK'

seed_genres = 'classical,country'

seed_tracks = '0c6xIDDpzE81m2q797ordA'

result = tracks_api.get_recommendations(
    limit=limit,
    market=market,
    seed_artists=seed_artists,
    seed_genres=seed_genres,
    seed_tracks=seed_tracks
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/exceptions/too-many-requests.md) |



