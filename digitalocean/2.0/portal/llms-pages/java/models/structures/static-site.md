# Static Site

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXRpY1NpdGU

*This model accepts additional fields of type Object.*


# Class Name

`StaticSite`


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
| `CatchallDocument` | `String` | Optional | The name of the document to use as the fallback for any requests to documents that are not found when serving this static site. Only 1 of `catchall_document` or `error_document` can be set. | String getCatchallDocument() | setCatchallDocument(String catchallDocument) |
| `Cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/cors.md) | Optional | - | Cors getCors() | setCors(Cors cors) |
| `ErrorDocument` | `String` | Optional | The name of the error document to use when serving this static site. Default: 404.html. If no such file exists within the built assets, App Platform will supply one.<br><br>**Default**: `"404.html"` | String getErrorDocument() | setErrorDocument(String errorDocument) |
| `IndexDocument` | `String` | Optional | The name of the index document to use when serving this static site. Default: index.html<br><br>**Default**: `"index.html"` | String getIndexDocument() | setIndexDocument(String indexDocument) |
| `OutputDir` | `String` | Optional | An optional path to where the built assets will be located, relative to the build context. If not set, App Platform will automatically scan for these directory names: `_static`, `dist`, `public`, `build`. | String getOutputDir() | setOutputDir(String outputDir) |
| `Routes` | [`List<ACriterionForRoutingHttpTrafficToAComponent>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. | List<ACriterionForRoutingHttpTrafficToAComponent> getRoutes() | setRoutes(List<ACriterionForRoutingHttpTrafficToAComponent> routes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Git;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.StaticSite;
import com.digitalocean.api.models.Type2;
import java.io.IOException;
import java.util.Arrays;

StaticSite staticSite = new StaticSite.Builder(
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
.catchallDocument("index.html")
.errorDocument("error.html")
.indexDocument("main.html")
.outputDir("dist/")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



