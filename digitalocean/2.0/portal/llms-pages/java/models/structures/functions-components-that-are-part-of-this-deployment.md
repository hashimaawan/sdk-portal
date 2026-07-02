# Functions Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZ1bmN0aW9ucyUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type Object.*


# Class Name

`FunctionsComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Namespace` | `String` | Optional | The namespace where the functions are deployed. | String getNamespace() | setNamespace(String namespace) |
| `SourceCommitHash` | `String` | Optional | The commit hash of the repository that was used to build this functions component. | String getSourceCommitHash() | setSourceCommitHash(String sourceCommitHash) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.FunctionsComponentsThatArePartOfThisDeployment;
import java.io.IOException;

FunctionsComponentsThatArePartOfThisDeployment functionsComponentsThatArePartOfThisDeployment = new FunctionsComponentsThatArePartOfThisDeployment.Builder()
    .name("my-functions-component")
    .namespace("ap-b2a93513-8d9b-4223-9d61-5e7272c81c32")
    .sourceCommitHash("54d4a727f457231062439895000d45437c7bb405")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



