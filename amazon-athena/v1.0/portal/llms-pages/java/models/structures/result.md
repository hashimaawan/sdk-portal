# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdA

*This model accepts additional fields of type Object.*


# Class Name

`Result`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StdOutS3Uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | String getStdOutS3Uri() | setStdOutS3Uri(String stdOutS3Uri) |
| `StdErrorS3Uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | String getStdErrorS3Uri() | setStdErrorS3Uri(String stdErrorS3Uri) |
| `ResultS3Uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | String getResultS3Uri() | setResultS3Uri(String resultS3Uri) |
| `ResultType` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` | String getResultType() | setResultType(String resultType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Result;
import java.io.IOException;

Result result = new Result.Builder()
    .stdOutS3Uri("StdOutS3Uri8")
    .stdErrorS3Uri("StdErrorS3Uri0")
    .resultS3Uri("ResultS3Uri4")
    .resultType("ResultType6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



