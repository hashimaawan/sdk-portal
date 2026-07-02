# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type Object.*


# Class Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TxtName` | `String` | Optional, Read-only | - | String getTxtName() | setTxtName(String txtName) |
| `TxtValue` | `String` | Optional, Read-only | - | String getTxtValue() | setTxtValue(String txtValue) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ListOfTxtValidationRecord;
import java.io.IOException;

ListOfTxtValidationRecord listOfTxtValidationRecord = new ListOfTxtValidationRecord.Builder()
    .txtName("_acme-challenge.app.example.com")
    .txtValue("lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



