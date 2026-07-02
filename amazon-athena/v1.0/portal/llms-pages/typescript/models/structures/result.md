# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdA


# Interface Name

`Result`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stdOutS3Uri` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `stdErrorS3Uri` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `resultS3Uri` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `resultType` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `\w+\/[-+.\w]+` |


# Example

```ts
import { Result } from 'amazon-athenalib';

const result: Result = {
  stdOutS3Uri: 'StdOutS3Uri8',
  stdErrorS3Uri: 'StdErrorS3Uri0',
  resultS3Uri: 'ResultS3Uri4',
  resultType: 'ResultType6',
};
```



