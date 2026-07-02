# Gitlab

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkdpdGxhYg

*This model accepts additional fields of type Object.*


# Class Name

`Gitlab`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Branch` | `String` | Optional | The name of the branch to use | String getBranch() | setBranch(String branch) |
| `DeployOnPush` | `Boolean` | Optional | Whether to automatically deploy new commits made to the repo | Boolean getDeployOnPush() | setDeployOnPush(Boolean deployOnPush) |
| `Repo` | `String` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` | String getRepo() | setRepo(String repo) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Gitlab;
import java.io.IOException;

Gitlab gitlab = new Gitlab.Builder()
    .branch("main")
    .deployOnPush(true)
    .repo("digitalocean/sample-golang")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



