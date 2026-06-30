# Me Episodes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRk1lJTI1MjBFcGlzb2RlcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`MeEpisodesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[str]` | Required | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). <br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.me_episodes_request import MeEpisodesRequest

me_episodes_request = MeEpisodesRequest(
    ids=[
        'ids3',
        'ids4',
        'ids5'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



