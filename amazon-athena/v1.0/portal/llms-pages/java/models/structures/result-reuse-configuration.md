# Result Reuse Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbg

Specifies the query result reuse behavior for the query.


# Class Name

`ResultReuseConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResultReuseByAgeConfiguration` | [`ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - | ResultReuseByAgeConfiguration2 getResultReuseByAgeConfiguration() | setResultReuseByAgeConfiguration(ResultReuseByAgeConfiguration2 resultReuseByAgeConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import com.amazonaws.useast1.athena.models.ResultReuseConfiguration;

ResultReuseConfiguration resultReuseConfiguration = new ResultReuseConfiguration.Builder()
    .resultReuseByAgeConfiguration(new ResultReuseByAgeConfiguration2.Builder(
        false
    )
    .maxAgeInMinutes(26)
    .build())
    .build();
```



