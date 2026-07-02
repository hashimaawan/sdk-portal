# Get Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetDataCatalogInput;
import java.io.IOException;

GetDataCatalogInput getDataCatalogInput = new GetDataCatalogInput.Builder(
    "Name6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



