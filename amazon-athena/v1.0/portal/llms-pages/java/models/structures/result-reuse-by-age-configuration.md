# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `boolean` | Required | - | boolean getEnabled() | setEnabled(boolean enabled) |
| `MaxAgeInMinutes` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 10080` | Integer getMaxAgeInMinutes() | setMaxAgeInMinutes(Integer maxAgeInMinutes) |


# Example

```java
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration;

ResultReuseByAgeConfiguration resultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration.Builder(
    false
)
.maxAgeInMinutes(134)
.build();
```



