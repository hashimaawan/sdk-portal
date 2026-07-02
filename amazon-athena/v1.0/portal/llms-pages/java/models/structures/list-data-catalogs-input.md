# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 2`, `<= 50` | Integer getMaxResults() | setMaxResults(Integer maxResults) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListDataCatalogsInput;

ListDataCatalogsInput listDataCatalogsInput = new ListDataCatalogsInput.Builder()
    .nextToken("NextToken8")
    .maxResults(50)
    .build();
```



