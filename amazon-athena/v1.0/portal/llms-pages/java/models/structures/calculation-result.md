# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StdOutS3Uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | String getStdOutS3Uri() | setStdOutS3Uri(String stdOutS3Uri) |
| `StdErrorS3Uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | String getStdErrorS3Uri() | setStdErrorS3Uri(String stdErrorS3Uri) |
| `ResultS3Uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | String getResultS3Uri() | setResultS3Uri(String resultS3Uri) |
| `ResultType` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` | String getResultType() | setResultType(String resultType) |


# Example

```java
import com.amazonaws.useast1.athena.models.CalculationResult;

CalculationResult calculationResult = new CalculationResult.Builder()
    .stdOutS3Uri("StdOutS3Uri4")
    .stdErrorS3Uri("StdErrorS3Uri6")
    .resultS3Uri("ResultS3Uri0")
    .resultType("ResultType2")
    .build();
```



