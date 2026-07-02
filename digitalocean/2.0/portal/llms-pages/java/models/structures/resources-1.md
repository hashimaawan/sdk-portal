# Resources 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc291cmNlczE

*This model accepts additional fields of type Object.*


# Class Name

`Resources1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AssignedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the project was created. | LocalDateTime getAssignedAt() | setAssignedAt(LocalDateTime assignedAt) |
| `Links` | [`Links4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links-4.md) | Optional | The links object contains the `self` object, which contains the resource relationship. | Links4 getLinks() | setLinks(Links4 links) |
| `Status` | [`Status14`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-14.md) | Optional | The status of assigning and fetching the resources. | Status14 getStatus() | setStatus(Status14 status) |
| `Urn` | `String` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` | String getUrn() | setUrn(String urn) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Links4;
import com.digitalocean.api.models.Resources1;
import com.digitalocean.api.models.Status14;
import java.io.IOException;

Resources1 resources1 = new Resources1.Builder()
    .assignedAt(DateTimeHelper.fromRfc8601DateTime("2018-09-28T19:26:37Z"))
    .links(new Links4.Builder()
        .self("self2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .status(Status14.OK)
    .urn("do:droplet:13457723")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



