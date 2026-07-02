# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).

*This model accepts additional fields of type Object.*


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `VarCharValue` | `String` | Optional | - | String getVarCharValue() | setVarCharValue(String varCharValue) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Datum;
import java.io.IOException;

Datum datum = new Datum.Builder()
    .varCharValue("VarCharValue8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



