# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.

*This model accepts additional fields of type Object.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `Integer` | Optional | Total number of items returned. | Integer getCount() | setCount(Integer count) |
| `Offset` | `Integer` | Optional | Position in pagination. | Integer getOffset() | setOffset(Integer offset) |
| `TotalCount` | `Integer` | Optional | Total number of items available. | Integer getTotalCount() | setTotalCount(Integer totalCount) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.giphy.api.ApiHelper;
import com.giphy.api.models.Pagination;
import java.io.IOException;

Pagination pagination = new Pagination.Builder()
    .count(25)
    .offset(75)
    .totalCount(250)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



