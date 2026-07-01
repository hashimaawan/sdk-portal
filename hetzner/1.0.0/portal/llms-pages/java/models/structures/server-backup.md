# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type Object.*


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Percentage` | `String` | Required | Percentage by how much the base price will increase | String getPercentage() | setPercentage(String percentage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServerBackup;
import java.io.IOException;

ServerBackup serverBackup = new ServerBackup.Builder(
    "20.0000000000"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



