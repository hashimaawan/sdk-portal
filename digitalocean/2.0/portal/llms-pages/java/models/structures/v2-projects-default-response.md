# V2 Projects Default Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2ProjectsDefaultResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Project` | [`Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/project.md) | Optional | - | Project getProject() | setProject(Project project) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Environment;
import com.digitalocean.api.models.Project;
import com.digitalocean.api.models.V2ProjectsDefaultResponse;
import java.io.IOException;
import java.util.UUID;

V2ProjectsDefaultResponse v2ProjectsDefaultResponse = new V2ProjectsDefaultResponse.Builder()
    .project(new Project.Builder()
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2017-10-19T21:44:20Z"))
        .description("Default project")
        .environment(Environment.DEVELOPMENT)
        .id(UUID.fromString("addb4547-6bab-419a-8542-76263a033cf6"))
        .name("Default")
        .ownerId(258992)
        .ownerUuid("99525febec065ca37b2ffe4f852fd2b2581895e7")
        .purpose("Just trying out DigitalOcean")
        .updatedAt(DateTimeHelper.fromRfc8601DateTime("2019-11-05T18:50:03Z"))
        .isDefault(true)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



