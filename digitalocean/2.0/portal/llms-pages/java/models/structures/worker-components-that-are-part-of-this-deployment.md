# Worker Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRldvcmtlciUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type Object.*


# Class Name

`WorkerComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `SourceCommitHash` | `String` | Optional | - | String getSourceCommitHash() | setSourceCommitHash(String sourceCommitHash) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.WorkerComponentsThatArePartOfThisDeployment;
import java.io.IOException;

WorkerComponentsThatArePartOfThisDeployment workerComponentsThatArePartOfThisDeployment = new WorkerComponentsThatArePartOfThisDeployment.Builder()
    .name("queue-runner")
    .sourceCommitHash("54d4a727f457231062439895000d45437c7bb405")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



