# Stop Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlN0b3BRdWVyeUV4ZWN1dGlvbg

<p>Stops a query execution. Requires you to have access to the workgroup in which the query ran.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="http://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


```ts
async stopQueryExecution(
  xAmzTarget: XAmzTarget50,
  body: StopQueryExecutionInput,
  xAmzContentSha256?: string,
  xAmzDate?: string,
  xAmzAlgorithm?: string,
  xAmzCredential?: string,
  xAmzSecurityToken?: string,
  xAmzSignature?: string,
  xAmzSignedHeaders?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<unknown | undefined>>
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget50`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/x-amz-target-50.md) | Header, Required | - |
| `body` | [`StopQueryExecutionInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/stop-query-execution-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string \| undefined` | Header, Optional | - |
| `xAmzDate` | `string \| undefined` | Header, Optional | - |
| `xAmzAlgorithm` | `string \| undefined` | Header, Optional | - |
| `xAmzCredential` | `string \| undefined` | Header, Optional | - |
| `xAmzSecurityToken` | `string \| undefined` | Header, Optional | - |
| `xAmzSignature` | `string \| undefined` | Header, Optional | - |
| `xAmzSignedHeaders` | `string \| undefined` | Header, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type `unknown`.


# Example Usage

```ts
const xAmzTarget = XAmzTarget50.EnumAmazonAthenaStopQueryExecution;

const body: StopQueryExecutionInput = {
  queryExecutionId: 'QueryExecutionId0',
};

try {
  const response = await api.stopQueryExecution(
    xAmzTarget,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiError` |
| 481 | InvalidRequestException | `ApiError` |



