# An App Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFuJTI1MjBhcHAlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type Object.*


# Class Name

`AnAppDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cause` | `String` | Optional | - | String getCause() | setCause(String cause) |
| `ClonedFrom` | `String` | Optional | - | String getClonedFrom() | setClonedFrom(String clonedFrom) |
| `CreatedAt` | `LocalDateTime` | Optional | - | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Functions` | [`List<FunctionsComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - | List<FunctionsComponentsThatArePartOfThisDeployment> getFunctions() | setFunctions(List<FunctionsComponentsThatArePartOfThisDeployment> functions) |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Jobs` | [`List<JobComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - | List<JobComponentsThatArePartOfThisDeployment> getJobs() | setJobs(List<JobComponentsThatArePartOfThisDeployment> jobs) |
| `Phase` | [`Phase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/phase.md) | Optional | **Default**: `Phase.UNKNOWN` | Phase getPhase() | setPhase(Phase phase) |
| `PhaseLastUpdatedAt` | `LocalDateTime` | Optional | - | LocalDateTime getPhaseLastUpdatedAt() | setPhaseLastUpdatedAt(LocalDateTime phaseLastUpdatedAt) |
| `Progress` | [`Progress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/progress.md) | Optional | - | Progress getProgress() | setProgress(Progress progress) |
| `Services` | [`List<ServiceComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - | List<ServiceComponentsThatArePartOfThisDeployment> getServices() | setServices(List<ServiceComponentsThatArePartOfThisDeployment> services) |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/app-spec.md) | Optional | The desired configuration of an application. | AppSpec getSpec() | setSpec(AppSpec spec) |
| `StaticSites` | [`List<StaticSiteComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - | List<StaticSiteComponentsThatArePartOfThisDeployment> getStaticSites() | setStaticSites(List<StaticSiteComponentsThatArePartOfThisDeployment> staticSites) |
| `TierSlug` | `String` | Optional, Read-only | - | String getTierSlug() | setTierSlug(String tierSlug) |
| `UpdatedAt` | `LocalDateTime` | Optional | - | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `Workers` | [`List<WorkerComponentsThatArePartOfThisDeployment>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - | List<WorkerComponentsThatArePartOfThisDeployment> getWorkers() | setWorkers(List<WorkerComponentsThatArePartOfThisDeployment> workers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.AnAppDeployment;
import com.digitalocean.api.models.FunctionsComponentsThatArePartOfThisDeployment;
import com.digitalocean.api.models.Phase;
import java.io.IOException;
import java.util.Arrays;

AnAppDeployment anAppDeployment = new AnAppDeployment.Builder()
    .cause("commit 9a4df0b pushed to github/digitalocean/sample-golang")
    .clonedFrom("3aa4d20e-5527-4c00-b496-601fbd22520a")
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-07-28T18:00:00Z"))
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
            .build()
    ))
    .id("b6bdf840-2854-4f87-a36c-5f231c617c84")
    .phase(Phase.ACTIVE)
    .phaseLastUpdatedAt(DateTimeHelper.fromRfc8601DateTime("0001-01-01T00:00:00Z"))
    .tierSlug("basic")
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2020-07-28T18:00:00Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



