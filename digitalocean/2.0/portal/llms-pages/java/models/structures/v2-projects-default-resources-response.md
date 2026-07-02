# V2 Projects Default Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2ProjectsDefaultResourcesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Resources` | [`List<Resources1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/resources-1.md) | Optional | - | List<Resources1> getResources() | setResources(List<Resources1> resources) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Links4;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.Resources1;
import com.digitalocean.api.models.Status14;
import com.digitalocean.api.models.V2ProjectsDefaultResourcesResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2ProjectsDefaultResourcesResponse v2ProjectsDefaultResourcesResponse = new V2ProjectsDefaultResourcesResponse.Builder(
    new Meta.Builder(
        2
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
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
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1")
                .next("next2")
            .additionalProperty("first", ApiHelper.deserialize("\"https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1\""))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



