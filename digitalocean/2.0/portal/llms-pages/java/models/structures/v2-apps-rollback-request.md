# V2 Apps Rollback Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsRollbackRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentId` | `String` | Optional | The ID of the deployment to rollback to. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `SkipPin` | `Boolean` | Optional | Whether to skip pinning the rollback deployment. If false, the rollback deployment will be pinned and any new deployments including Auto Deploy on Push hooks will be disabled until the rollback is either manually committed or reverted via the CommitAppRollback or RevertAppRollback endpoints respectively. If true, the rollback will be immediately committed and the app will remain unpinned. | Boolean getSkipPin() | setSkipPin(Boolean skipPin) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2AppsRollbackRequest;
import java.io.IOException;

V2AppsRollbackRequest v2AppsRollbackRequest = new V2AppsRollbackRequest.Builder()
    .deploymentId("3aa4d20e-5527-4c00-b496-601fbd22520a")
    .skipPin(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



