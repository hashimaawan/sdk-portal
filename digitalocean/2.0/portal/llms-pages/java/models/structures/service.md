# Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZpY2U

*This model accepts additional fields of type Object.*


# Class Name

`Service`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BuildCommand` | `String` | Optional | An optional build command to run while building this component from source. | String getBuildCommand() | setBuildCommand(String buildCommand) |
| `DockerfilePath` | `String` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. | String getDockerfilePath() | setDockerfilePath(String dockerfilePath) |
| `EnvironmentSlug` | `String` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). | String getEnvironmentSlug() | setEnvironmentSlug(String environmentSlug) |
| `Envs` | [`List<Env>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/env.md) | Optional | A list of environment variables made available to the component. | List<Env> getEnvs() | setEnvs(List<Env> envs) |
| `Git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/git.md) | Optional | - | Git getGit() | setGit(Git git) |
| `Github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/github.md) | Optional | - | Github getGithub() | setGithub(Github github) |
| `Gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/gitlab.md) | Optional | - | Gitlab getGitlab() | setGitlab(Gitlab gitlab) |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/image.md) | Optional | - | Image getImage() | setImage(Image image) |
| `LogDestinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/configurations-for-external-logging.md) | Optional | - | ConfigurationsForExternalLogging getLogDestinations() | setLogDestinations(ConfigurationsForExternalLogging logDestinations) |
| `Name` | `String` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | String getName() | setName(String name) |
| `RunCommand` | `String` | Optional | An optional run command to override the component's default. | String getRunCommand() | setRunCommand(String runCommand) |
| `SourceDir` | `String` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. | String getSourceDir() | setSourceDir(String sourceDir) |
| `InstanceCount` | `Long` | Optional | The amount of instances that this component should be scaled to. Default: 1<br><br>**Default**: `1L`<br><br>**Constraints**: `>= 1` | Long getInstanceCount() | setInstanceCount(Long instanceCount) |
| `InstanceSizeSlug` | [`InstanceSizeSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/instance-size-slug.md) | Optional | The instance size to use for this component. Default: `basic-xxs`<br><br>**Default**: `InstanceSizeSlug.BASICXXS` | InstanceSizeSlug getInstanceSizeSlug() | setInstanceSizeSlug(InstanceSizeSlug instanceSizeSlug) |
| `Cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/cors.md) | Optional | - | Cors getCors() | setCors(Cors cors) |
| `HealthCheck` | [`HealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/health-check.md) | Optional | - | HealthCheck getHealthCheck() | setHealthCheck(HealthCheck healthCheck) |
| `HttpPort` | `Long` | Optional | The internal port on which this service's run command will listen. Default: 8080<br>If there is not an environment variable with the name `PORT`, one will be automatically added with its value set to the value of this field.<br><br>**Constraints**: `>= 1`, `<= 65535` | Long getHttpPort() | setHttpPort(Long httpPort) |
| `InternalPorts` | `List<Long>` | Optional | The ports on which this service will listen for internal traffic. | List<Long> getInternalPorts() | setInternalPorts(List<Long> internalPorts) |
| `Routes` | [`List<ACriterionForRoutingHttpTrafficToAComponent>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. | List<ACriterionForRoutingHttpTrafficToAComponent> getRoutes() | setRoutes(List<ACriterionForRoutingHttpTrafficToAComponent> routes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Git;
import com.digitalocean.api.models.InstanceSizeSlug;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.Service;
import com.digitalocean.api.models.Type2;
import java.io.IOException;
import java.util.Arrays;

Service service = new Service.Builder(
    "api"
)
.buildCommand("npm run build")
.dockerfilePath("path/to/Dockerfile")
.environmentSlug("node-js")
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
.runCommand("bin/api")
.sourceDir("path/to/dir")
.instanceCount(2L)
.instanceSizeSlug(InstanceSizeSlug.BASICXXS)
.httpPort(3000L)
.internalPorts(Arrays.asList(
        80L,
        443L
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



