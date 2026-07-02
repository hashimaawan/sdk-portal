# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Projects` | [`List<Project>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/project.md) | Optional | - | List<Project> getProjects() | setProjects(List<Project> projects) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Environment;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.Project;
import com.digitalocean.api.models.V2ProjectsResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2ProjectsResponse v2ProjectsResponse = new V2ProjectsResponse.Builder(
    new Meta.Builder(
        2
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.projects(Arrays.asList(
        new Project.Builder()
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2018-09-27T20:10:35Z"))
            .description("My website API")
            .environment(Environment.PRODUCTION)
            .id(UUID.fromString("4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679"))
            .name("my-web-api")
            .ownerId(258992)
            .ownerUuid("99525febec065ca37b2ffe4f852fd2b2581895e7")
            .purpose("Service or API")
            .updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-09-27T20:10:35Z"))
            .isDefault(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Project.Builder()
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
            .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/projects?page=1")
                .next("next2")
            .additionalProperty("first", ApiHelper.deserialize("\"https://api.digitalocean.com/v2/projects?page=1\""))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



