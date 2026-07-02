# Member

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk1lbWJlcg

*This model accepts additional fields of type Object.*


# Class Name

`Member`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional | A time value given in ISO8601 combined date and time format that represents when the resource was created. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Name` | `String` | Optional | The name of the resource. | String getName() | setName(String name) |
| `Urn` | `String` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` | String getUrn() | setUrn(String urn) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Member;
import java.io.IOException;

Member member = new Member.Builder()
    .createdAt("2020-03-13T19:30:48Z")
    .name("nyc1-load-balancer-01")
    .urn("do:droplet:13457723")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



