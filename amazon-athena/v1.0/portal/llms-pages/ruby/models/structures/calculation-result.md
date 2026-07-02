# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `std_out_s_3_uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `std_error_s_3_uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `result_s_3_uri` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `result_type` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
calculation_result = CalculationResult.new(
  std_out_s3_uri: 'StdOutS3Uri0',
  std_error_s3_uri: 'StdErrorS3Uri2',
  result_s3_uri: 'ResultS3Uri4',
  result_type: 'ResultType8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



