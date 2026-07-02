# V2 Projects Default Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2ProjectsDefaultResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Resources` | `List<String>` | Optional | A list of uniform resource names (URNs) to be added to a project.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` | List<String> getResources() | setResources(List<String> resources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2ProjectsDefaultResourcesRequest;
import java.io.IOException;
import java.util.Arrays;

V2ProjectsDefaultResourcesRequest v2ProjectsDefaultResourcesRequest = new V2ProjectsDefaultResourcesRequest.Builder()
    .resources(Arrays.asList(
        "do:droplet:13457723"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



