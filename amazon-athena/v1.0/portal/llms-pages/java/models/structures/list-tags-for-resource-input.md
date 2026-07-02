# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA


# Class Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceARN` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | String getResourceARN() | setResourceARN(String resourceARN) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 75` | Integer getMaxResults() | setMaxResults(Integer maxResults) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListTagsForResourceInput;

ListTagsForResourceInput listTagsForResourceInput = new ListTagsForResourceInput.Builder(
    "ResourceARN0"
)
.nextToken("NextToken0")
.maxResults(76)
.build();
```



