# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StdOutS3Uri` | `*string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `StdErrorS3Uri` | `*string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `ResultS3Uri` | `*string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `ResultType` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    calculationResult := models.CalculationResult{
        StdOutS3Uri:          models.ToPointer("StdOutS3Uri4"),
        StdErrorS3Uri:        models.ToPointer("StdErrorS3Uri6"),
        ResultS3Uri:          models.ToPointer("ResultS3Uri0"),
        ResultType:           models.ToPointer("ResultType2"),
    }

}
```



