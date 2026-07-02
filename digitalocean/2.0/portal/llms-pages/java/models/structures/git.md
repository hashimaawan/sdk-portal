# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type Object.*


# Class Name

`Git`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Branch` | `String` | Optional | The name of the branch to use | String getBranch() | setBranch(String branch) |
| `RepoCloneUrl` | `String` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` | String getRepoCloneUrl() | setRepoCloneUrl(String repoCloneUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Git;
import java.io.IOException;

Git git = new Git.Builder()
    .branch("main")
    .repoCloneUrl("https://github.com/digitalocean/sample-golang.git")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



