# V2 Apps Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `App` | [`AListOfApp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/a-list-of-app.md) | Optional | An application's configuration and status. | AListOfApp getApp() | setApp(AListOfApp app) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.AListOfApp;
import com.digitalocean.api.models.Alert;
import com.digitalocean.api.models.AnAppDeployment;
import com.digitalocean.api.models.AppSpec;
import com.digitalocean.api.models.ContainsAllDomainsForTheApp;
import com.digitalocean.api.models.Cors;
import com.digitalocean.api.models.Database;
import com.digitalocean.api.models.Domain;
import com.digitalocean.api.models.Engine;
import com.digitalocean.api.models.Env;
import com.digitalocean.api.models.Function;
import com.digitalocean.api.models.FunctionsComponentsThatArePartOfThisDeployment;
import com.digitalocean.api.models.Git;
import com.digitalocean.api.models.Github;
import com.digitalocean.api.models.Job;
import com.digitalocean.api.models.MinimumTlsVersion;
import com.digitalocean.api.models.Operator;
import com.digitalocean.api.models.Phase1;
import com.digitalocean.api.models.Progress1;
import com.digitalocean.api.models.Region1;
import com.digitalocean.api.models.Rule;
import com.digitalocean.api.models.Scope;
import com.digitalocean.api.models.Type1;
import com.digitalocean.api.models.Type2;
import com.digitalocean.api.models.V2AppsResponse1;
import com.digitalocean.api.models.Window;
import java.io.IOException;
import java.util.Arrays;

V2AppsResponse1 v2AppsResponse1 = new V2AppsResponse1.Builder()
    .app(new AListOfApp.Builder(
        new AppSpec.Builder(
            "name2"
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
                .build()
            ))
        .region(Region1.BLR)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .activeDeployment(new AnAppDeployment.Builder()
            .cause("cause6")
            .clonedFrom("cloned_from2")
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .functions(Arrays.asList(
                new FunctionsComponentsThatArePartOfThisDeployment.Builder()
                    .name("name4")
                    .namespace("namespace8")
                    .sourceCommitHash("source_commit_hash4")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new FunctionsComponentsThatArePartOfThisDeployment.Builder()
                    .name("name4")
                    .namespace("namespace8")
                    .sourceCommitHash("source_commit_hash4")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new FunctionsComponentsThatArePartOfThisDeployment.Builder()
                    .name("name4")
                    .namespace("namespace8")
                    .sourceCommitHash("source_commit_hash4")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
            .id("id0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .defaultIngress("default_ingress8")
    .domains(Arrays.asList(
            new ContainsAllDomainsForTheApp.Builder()
                .certificateExpiresAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .id("id0")
                .phase(Phase1.CONFIGURING)
                .progress(new Progress1.Builder()
                    .steps(Arrays.asList(
                        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .rotateValidationRecords(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .id("id2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



