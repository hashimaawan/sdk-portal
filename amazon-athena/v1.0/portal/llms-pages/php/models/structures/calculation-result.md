# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.

*This model accepts additional fields of type array.*


# Class Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `stdOutS3Uri` | `?string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | getStdOutS3Uri(): ?string | setStdOutS3Uri(?string stdOutS3Uri): void |
| `stdErrorS3Uri` | `?string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | getStdErrorS3Uri(): ?string | setStdErrorS3Uri(?string stdErrorS3Uri): void |
| `resultS3Uri` | `?string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | getResultS3Uri(): ?string | setResultS3Uri(?string resultS3Uri): void |
| `resultType` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` | getResultType(): ?string | setResultType(?string resultType): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CalculationResultBuilder;
use AmazonAthenaLib\ApiHelper;

$calculationResult = CalculationResultBuilder::init()
    ->stdOutS3Uri('StdOutS3Uri4')
    ->stdErrorS3Uri('StdErrorS3Uri6')
    ->resultS3Uri('ResultS3Uri0')
    ->resultType('ResultType2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



