# Function

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZ1bmN0aW9u

*This model accepts additional fields of type Object.*


# Class Name

`Function`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Alerts` | [`List<Alert>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/alert.md) | Optional | - | List<Alert> getAlerts() | setAlerts(List<Alert> alerts) |
| `Cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/cors.md) | Optional | - | Cors getCors() | setCors(Cors cors) |
| `Envs` | [`List<Env>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/env.md) | Optional | A list of environment variables made available to the component. | List<Env> getEnvs() | setEnvs(List<Env> envs) |
| `Git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/git.md) | Optional | - | Git getGit() | setGit(Git git) |
| `Github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/github.md) | Optional | - | Github getGithub() | setGithub(Github github) |
| `Gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/gitlab.md) | Optional | - | Gitlab getGitlab() | setGitlab(Gitlab gitlab) |
| `LogDestinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/configurations-for-external-logging.md) | Optional | - | ConfigurationsForExternalLogging getLogDestinations() | setLogDestinations(ConfigurationsForExternalLogging logDestinations) |
| `Name` | `String` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | String getName() | setName(String name) |
| `Routes` | [`List<ACriterionForRoutingHttpTrafficToAComponent>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. | List<ACriterionForRoutingHttpTrafficToAComponent> getRoutes() | setRoutes(List<ACriterionForRoutingHttpTrafficToAComponent> routes) |
| `SourceDir` | `String` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. | String getSourceDir() | setSourceDir(String sourceDir) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Alert;
import com.digitalocean.api.models.Cors;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Function;
import com.digitalocean.api.models.Git;
import com.digitalocean.api.models.Github;
import com.digitalocean.api.models.Operator;
import com.digitalocean.api.models.Rule;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.Type2;
import com.digitalocean.api.models.Window;
import java.io.IOException;
import java.util.Arrays;

Function function = new Function.Builder(
    "api"
)
.alerts(Arrays.asList(
        new Alert.Builder()
            .disabled(false)
            .operator(Operator.LESS_THAN)
            .rule(Rule.MEM_UTILIZATION)
            .value(12.58D)
            .window(Window.THIRTY_MINUTES)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Alert.Builder()
            .disabled(false)
            .operator(Operator.LESS_THAN)
            .rule(Rule.MEM_UTILIZATION)
            .value(12.58D)
            .window(Window.THIRTY_MINUTES)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.cors(new Cors.Builder()
        .allowCredentials(false)
        .allowHeaders(Arrays.asList(
            "allow_headers9",
            "allow_headers0"
        ))
        .allowMethods(Arrays.asList(
            "allow_methods8",
            "allow_methods9",
            "allow_methods0"
        ))
        .allowOrigins(Arrays.asList(
            null
        ))
        .exposeHeaders(Arrays.asList(
            "expose_headers2"
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.envs(Arrays.asList(
        new Env.Builder(
            "key2"
        )
        .scope(Scope.UNSET)
        .type(Type2.GENERAL)
        .value("value4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.git(new Git.Builder()
        .branch("branch8")
        .repoCloneUrl("repo_clone_url8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.github(new Github.Builder()
        .branch("branch4")
        .deployOnPush(false)
        .repo("repo6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.sourceDir("path/to/dir")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



