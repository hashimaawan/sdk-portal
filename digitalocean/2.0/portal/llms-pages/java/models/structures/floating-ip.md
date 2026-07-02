# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

An objects containing information about a resource associated with a Droplet.

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cost` | `String` | Optional | The cost of the resource in USD per month if the resource is retained after the Droplet is destroyed. | String getCost() | setCost(String cost) |
| `Id` | `String` | Optional | The unique identifier for the resource associated with the Droplet. | String getId() | setId(String id) |
| `Name` | `String` | Optional | The name of the resource associated with the Droplet. | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.FloatingIp;
import java.io.IOException;

FloatingIp floatingIp = new FloatingIp.Builder()
    .cost("0.05")
    .id("61486916")
    .name("ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



