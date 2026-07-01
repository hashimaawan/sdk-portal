# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

*This model accepts additional fields of type Object.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LastPage` | `Double` | Required | ID of the last page available. Can be null if the current page is the last one. | Double getLastPage() | setLastPage(Double lastPage) |
| `NextPage` | `Double` | Required | ID of the next page. Can be null if the current page is the last one. | Double getNextPage() | setNextPage(Double nextPage) |
| `Page` | `double` | Required | Current page number | double getPage() | setPage(double page) |
| `PerPage` | `double` | Required | Maximum number of items shown per page in the response | double getPerPage() | setPerPage(double perPage) |
| `PreviousPage` | `Double` | Required | ID of the previous page. Can be null if the current page is the first one. | Double getPreviousPage() | setPreviousPage(Double previousPage) |
| `TotalEntries` | `Double` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. | Double getTotalEntries() | setTotalEntries(Double totalEntries) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Pagination;
import java.io.IOException;

Pagination pagination = new Pagination.Builder(
    4D,
    4D,
    3D,
    25D,
    2D,
    100D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



