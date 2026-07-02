# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.

*This model accepts additional fields of type Any.*


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `std_out_s_3_uri` | `str` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `std_error_s_3_uri` | `str` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `result_s_3_uri` | `str` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `result_type` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.calculation_result import CalculationResult

calculation_result = CalculationResult(
    std_out_s_3_uri='StdOutS3Uri0',
    std_error_s_3_uri='StdErrorS3Uri2',
    result_s_3_uri='ResultS3Uri4',
    result_type='ResultType8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



