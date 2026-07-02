# V2 Apps Deployments Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsDeploymentsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/an-app-deployment.md) | Optional | - | AnAppDeployment getDeployment() | setDeployment(AnAppDeployment deployment) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.AnAppDeployment;
import com.digitalocean.api.models.FunctionsComponentsThatArePartOfThisDeployment;
import com.digitalocean.api.models.V2AppsDeploymentsResponse1;
import java.io.IOException;
import java.util.Arrays;

V2AppsDeploymentsResponse1 v2AppsDeploymentsResponse1 = new V2AppsDeploymentsResponse1.Builder()
    .deployment(new AnAppDeployment.Builder()
        .cause("cause8")
        .clonedFrom("cloned_from0")
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .functions(Arrays.asList(
            new FunctionsComponentsThatArePartOfThisDeployment.Builder()
                .name("name4")
                .namespace("namespace8")
                .sourceCommitHash("source_commit_hash4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .id("id2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



