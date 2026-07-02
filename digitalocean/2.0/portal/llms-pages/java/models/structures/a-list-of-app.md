# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type Object.*


# Class Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ActiveDeployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/an-app-deployment.md) | Optional | - | AnAppDeployment getActiveDeployment() | setActiveDeployment(AnAppDeployment activeDeployment) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DefaultIngress` | `String` | Optional, Read-only | - | String getDefaultIngress() | setDefaultIngress(String defaultIngress) |
| `Domains` | [`List<ContainsAllDomainsForTheApp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - | List<ContainsAllDomainsForTheApp> getDomains() | setDomains(List<ContainsAllDomainsForTheApp> domains) |
| `Id` | `String` | Optional, Read-only | - | String getId() | setId(String id) |
| `InProgressDeployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/an-app-deployment.md) | Optional | - | AnAppDeployment getInProgressDeployment() | setInProgressDeployment(AnAppDeployment inProgressDeployment) |
| `LastDeploymentCreatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getLastDeploymentCreatedAt() | setLastDeploymentCreatedAt(LocalDateTime lastDeploymentCreatedAt) |
| `LiveDomain` | `String` | Optional, Read-only | - | String getLiveDomain() | setLiveDomain(String liveDomain) |
| `LiveUrl` | `String` | Optional, Read-only | - | String getLiveUrl() | setLiveUrl(String liveUrl) |
| `LiveUrlBase` | `String` | Optional, Read-only | - | String getLiveUrlBase() | setLiveUrlBase(String liveUrlBase) |
| `OwnerUuid` | `String` | Optional, Read-only | - | String getOwnerUuid() | setOwnerUuid(String ownerUuid) |
| `PendingDeployment` | [`PendingDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pending-deployment.md) | Optional | - | PendingDeployment getPendingDeployment() | setPendingDeployment(PendingDeployment pendingDeployment) |
| `PinnedDeployment` | [`PinnedDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pinned-deployment.md) | Optional | - | PinnedDeployment getPinnedDeployment() | setPinnedDeployment(PinnedDeployment pinnedDeployment) |
| `ProjectId` | `String` | Optional, Read-only | - | String getProjectId() | setProjectId(String projectId) |
| `Region` | [`GeographicalInformationAboutAnAppOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/geographical-information-about-an-app-origin.md) | Optional | - | GeographicalInformationAboutAnAppOrigin getRegion() | setRegion(GeographicalInformationAboutAnAppOrigin region) |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/app-spec.md) | Required | The desired configuration of an application. | AppSpec getSpec() | setSpec(AppSpec spec) |
| `TierSlug` | `String` | Optional, Read-only | - | String getTierSlug() | setTierSlug(String tierSlug) |
| `UpdatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
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
import com.digitalocean.api.models.Window;
import java.io.IOException;
import java.util.Arrays;

AListOfApp aListOfApp = new AListOfApp.Builder(
    new AppSpec.Builder(
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
    .region(Region1.NYC)
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
.createdAt(DateTimeHelper.fromRfc8601DateTime("2020-11-19T20:27:18Z"))
.defaultIngress("digitalocean.com")
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
.id("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf")
.lastDeploymentCreatedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-19T20:27:18Z"))
.liveDomain("live_domain")
.liveUrl("google.com")
.liveUrlBase("digitalocean.com")
.ownerUuid("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf")
.projectId("88b72d1a-b78a-4d9f-9090-b53c4399073f")
.tierSlug("basic")
.updatedAt(DateTimeHelper.fromRfc8601DateTime("2020-12-01T00:42:16Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



