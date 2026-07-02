# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`DeleteNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getNamedQueryId() | setNamedQueryId(String namedQueryId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.DeleteNamedQueryInput;
import java.io.IOException;

DeleteNamedQueryInput deleteNamedQueryInput = new DeleteNamedQueryInput.Builder(
    "NamedQueryId4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



