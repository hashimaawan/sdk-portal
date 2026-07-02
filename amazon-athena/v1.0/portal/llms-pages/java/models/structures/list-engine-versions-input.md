# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 10` | Integer getMaxResults() | setMaxResults(Integer maxResults) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListEngineVersionsInput;

ListEngineVersionsInput listEngineVersionsInput = new ListEngineVersionsInput.Builder()
    .nextToken("NextToken6")
    .maxResults(10)
    .build();
```



