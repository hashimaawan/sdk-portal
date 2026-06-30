# Me Shows Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRk1lJTI1MjBTaG93cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`MeShowsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ids` | `List<String>` | Optional | A JSON array of the [Spotify IDs](https://developer.spotify.com/documentation/web-api/#spotify-uris-and-ids).  <br>A maximum of 50 items can be specified in one request. *Note: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored.* | List<String> getIds() | setIds(List<String> ids) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.spotify.api.ApiHelper;
import com.spotify.api.models.MeShowsRequest;
import java.io.IOException;
import java.util.Arrays;

MeShowsRequest meShowsRequest = new MeShowsRequest.Builder()
    .ids(Arrays.asList(
        "ids7"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



