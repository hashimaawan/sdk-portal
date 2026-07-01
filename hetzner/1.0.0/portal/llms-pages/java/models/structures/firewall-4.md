# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type Object.*


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Firewall` | `Integer` | Optional | ID of the Firewall | Integer getFirewall() | setFirewall(Integer firewall) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Firewall4;
import java.io.IOException;

Firewall4 firewall4 = new Firewall4.Builder()
    .firewall(176)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



