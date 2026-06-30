# Me following Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRk1lJTI1MjBGb2xsb3dpbmclMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type Object.*


# Class Name

`MeFollowingRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ids` | `List<String>` | Optional | A JSON array of the artist or user [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `{ids:["74ASZWbe4lXaubB36ztrGX", "08td7MxkoHQkXnWAYD8d6Q"]}`. A maximum of 50 IDs can be sent in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ | List<String> getIds() | setIds(List<String> ids) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.MeFollowingRequest1;
import java.io.IOException;
import java.util.Arrays;

MeFollowingRequest1 meFollowingRequest1 = new MeFollowingRequest1.Builder()
    .ids(Arrays.asList(
        "ids5",
        "ids6"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



