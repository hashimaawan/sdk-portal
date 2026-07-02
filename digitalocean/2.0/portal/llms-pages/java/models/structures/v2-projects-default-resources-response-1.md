# V2 Projects Default Resources Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2ProjectsDefaultResourcesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Resources` | [`List<Resources1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/resources-1.md) | Optional | - | List<Resources1> getResources() | setResources(List<Resources1> resources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Links4;
import com.digitalocean.api.models.Resources1;
import com.digitalocean.api.models.Status14;
import com.digitalocean.api.models.V2ProjectsDefaultResourcesResponse1;
import java.io.IOException;
import java.util.Arrays;

V2ProjectsDefaultResourcesResponse1 v2ProjectsDefaultResourcesResponse1 = new V2ProjectsDefaultResourcesResponse1.Builder()
    .resources(Arrays.asList(
        new Resources1.Builder()
            .assignedAt(DateTimeHelper.fromRfc8601DateTime("2018-09-28T19:26:37Z"))
            .links(new Links4.Builder()
                .self("https://api.digitalocean.com/v2/droplets/13457723")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .status(Status14.OK)
            .urn("do:droplet:13457723")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Resources1.Builder()
            .assignedAt(DateTimeHelper.fromRfc8601DateTime("2019-03-31T16:24:14Z"))
            .links(new Links4.Builder()
                .self("https://api.digitalocean.com/v2/domains/example.com")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .status(Status14.OK)
            .urn("do:domain:example.com")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



