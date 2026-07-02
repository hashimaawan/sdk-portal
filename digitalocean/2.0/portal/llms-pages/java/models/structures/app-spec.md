# App Spec

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFwcFNwZWM

The desired configuration of an application.

*This model accepts additional fields of type Object.*


# Class Name

`AppSpec`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Databases` | [`List<Database>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/database.md) | Optional | Database instances which can provide persistence to workloads within the<br>application. | List<Database> getDatabases() | setDatabases(List<Database> databases) |
| `Domains` | [`List<Domain>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/domain.md) | Optional | A set of hostnames where the application will be available. | List<Domain> getDomains() | setDomains(List<Domain> domains) |
| `Functions` | [`List<Function>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/function.md) | Optional | Workloads which expose publicly-accessible HTTP services via Functions Components. | List<Function> getFunctions() | setFunctions(List<Function> functions) |
| `Jobs` | [`List<Job>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/job.md) | Optional | Pre and post deployment workloads which do not expose publicly-accessible HTTP routes. | List<Job> getJobs() | setJobs(List<Job> jobs) |
| `Name` | `String` | Required | The name of the app. Must be unique across all apps in the same account.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | String getName() | setName(String name) |
| `Region` | [`Region1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-1.md) | Optional | The slug form of the geographical origin of the app. Default: `nearest available` | Region1 getRegion() | setRegion(Region1 region) |
| `Services` | [`List<Service>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/service.md) | Optional | Workloads which expose publicly-accessible HTTP services. | List<Service> getServices() | setServices(List<Service> services) |
| `StaticSites` | [`List<StaticSite>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/static-site.md) | Optional | Content which can be rendered to static web assets. | List<StaticSite> getStaticSites() | setStaticSites(List<StaticSite> staticSites) |
| `Workers` | [`List<Worker>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/worker.md) | Optional | Workloads which do not expose publicly-accessible HTTP services. | List<Worker> getWorkers() | setWorkers(List<Worker> workers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Alert;
import com.digitalocean.api.models.AppSpec;
import com.digitalocean.api.models.Cors;
import com.digitalocean.api.models.Database;
import com.digitalocean.api.models.Domain;
import com.digitalocean.api.models.Engine;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Function;
import com.digitalocean.api.models.Git;
import com.digitalocean.api.models.Github;
import com.digitalocean.api.models.Job;
import com.digitalocean.api.models.MinimumTlsVersion;
import com.digitalocean.api.models.Operator;
import com.digitalocean.api.models.Region1;
import com.digitalocean.api.models.Rule;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.Type1;
import com.digitalocean.api.models.Type2;
import com.digitalocean.api.models.Window;
import java.io.IOException;
import java.util.Arrays;

AppSpec appSpec = new AppSpec.Builder(
    "web-app-01"
)
.databases(Arrays.asList(
        new Database.Builder(
            "name6"
        )
        .clusterName("cluster_name8")
        .dbName("db_name0")
        .dbUser("db_user8")
        .engine(Engine.PG)
        .production(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Database.Builder(
            "name6"
        )
        .clusterName("cluster_name8")
        .dbName("db_name0")
        .dbUser("db_user8")
        .engine(Engine.PG)
        .production(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.domains(Arrays.asList(
        new Domain.Builder(
            "domain6"
        )
        .minimumTlsVersion(MinimumTlsVersion.ENUM_12)
        .type(Type1.PRIMARY)
        .wildcard(false)
        .zone("zone2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Domain.Builder(
            "domain6"
        )
        .minimumTlsVersion(MinimumTlsVersion.ENUM_12)
        .type(Type1.PRIMARY)
        .wildcard(false)
        .zone("zone2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Domain.Builder(
            "domain6"
        )
        .minimumTlsVersion(MinimumTlsVersion.ENUM_12)
        .type(Type1.PRIMARY)
        .wildcard(false)
        .zone("zone2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.functions(Arrays.asList(
        new Function.Builder(
            "name4"
        )
        .alerts(Arrays.asList(
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
        .github(new Github.Builder()
                .branch("branch4")
                .deployOnPush(false)
                .repo("repo6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Function.Builder(
            "name4"
        )
        .alerts(Arrays.asList(
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
        .github(new Github.Builder()
                .branch("branch4")
                .deployOnPush(false)
                .repo("repo6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.jobs(Arrays.asList(
        new Job.Builder(
            "name4"
        )
        .buildCommand("build_command8")
        .dockerfilePath("dockerfile_path6")
        .environmentSlug("environment_slug2")
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Job.Builder(
            "name4"
        )
        .buildCommand("build_command8")
        .dockerfilePath("dockerfile_path6")
        .environmentSlug("environment_slug2")
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.region(Region1.NYC)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



