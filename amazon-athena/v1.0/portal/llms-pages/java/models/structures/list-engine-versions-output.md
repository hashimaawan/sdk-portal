# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EngineVersions` | [`List<EngineVersion>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` | List<EngineVersion> getEngineVersions() | setEngineVersions(List<EngineVersion> engineVersions) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.EngineVersion;
import com.amazonaws.useast1.athena.models.ListEngineVersionsOutput;
import java.io.IOException;
import java.util.Arrays;

ListEngineVersionsOutput listEngineVersionsOutput = new ListEngineVersionsOutput.Builder()
    .engineVersions(Arrays.asList(
        new EngineVersion.Builder()
            .selectedEngineVersion("SelectedEngineVersion2")
            .effectiveEngineVersion("EffectiveEngineVersion2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



