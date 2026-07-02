# Calculation Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uUmVzdWx0

Contains information about an application-specific calculation result.

*This model accepts additional fields of type unknown.*


# Interface Name

`CalculationResult`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stdOutS3Uri` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `stdErrorS3Uri` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `resultS3Uri` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `resultType` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CalculationResult } from 'amazon-athenalib';

const calculationResult: CalculationResult = {
  stdOutS3Uri: 'StdOutS3Uri4',
  stdErrorS3Uri: 'StdErrorS3Uri6',
  resultS3Uri: 'ResultS3Uri0',
  resultType: 'ResultType2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



