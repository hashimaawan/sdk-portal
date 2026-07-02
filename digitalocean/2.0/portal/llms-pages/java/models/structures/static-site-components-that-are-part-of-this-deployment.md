# Static Site Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXRpYyUyNTIwU2l0ZSUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type Object.*


# Class Name

`StaticSiteComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `SourceCommitHash` | `String` | Optional | - | String getSourceCommitHash() | setSourceCommitHash(String sourceCommitHash) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.StaticSiteComponentsThatArePartOfThisDeployment;
import java.io.IOException;

StaticSiteComponentsThatArePartOfThisDeployment staticSiteComponentsThatArePartOfThisDeployment = new StaticSiteComponentsThatArePartOfThisDeployment.Builder()
    .name("web")
    .sourceCommitHash("54d4a727f457231062439895000d45437c7bb405")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



