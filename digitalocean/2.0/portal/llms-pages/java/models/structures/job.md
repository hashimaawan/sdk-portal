# Job

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkpvYg

*This model accepts additional fields of type Object.*


# Class Name

`Job`


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
| `Kind` | [`Kind`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/kind.md) | Optional | - UNSPECIFIED: Default job type, will auto-complete to POST_DEPLOY kind.<br>- PRE_DEPLOY: Indicates a job that runs before an app deployment.<br>- POST_DEPLOY: Indicates a job that runs after an app deployment.<br>- FAILED_DEPLOY: Indicates a job that runs after a component fails to deploy.<br><br>**Default**: `Kind.UNSPECIFIED` | Kind getKind() | setKind(Kind kind) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Git;
import com.digitalocean.api.models.InstanceSizeSlug;
import com.digitalocean.api.models.Job;
import com.digitalocean.api.models.Kind;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.Type2;
import java.io.IOException;
import java.util.Arrays;

Job job = new Job.Builder(
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
        .build(),
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
.kind(Kind.PRE_DEPLOY)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



