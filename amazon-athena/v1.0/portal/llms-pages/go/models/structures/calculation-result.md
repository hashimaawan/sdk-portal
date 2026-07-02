# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.

*This model accepts additional fields of type interface{}.*


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StdOutS3Uri` | `*string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `StdErrorS3Uri` | `*string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `ResultS3Uri` | `*string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `ResultType` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    calculationResult := models.CalculationResult{
        StdOutS3Uri:           models.ToPointer("StdOutS3Uri4"),
        StdErrorS3Uri:         models.ToPointer("StdErrorS3Uri6"),
        ResultS3Uri:           models.ToPointer("ResultS3Uri0"),
        ResultType:            models.ToPointer("ResultType2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



