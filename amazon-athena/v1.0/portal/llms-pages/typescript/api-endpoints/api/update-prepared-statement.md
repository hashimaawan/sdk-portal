# Update Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlVwZGF0ZVByZXBhcmVkU3RhdGVtZW50

Updates a prepared statement.

```ts
async updatePreparedStatement(
  xAmzTarget: XAmzTarget58,
  body: UpdatePreparedStatementInput,
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
| `xAmzTarget` | [`XAmzTarget58`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/x-amz-target-58.md) | Header, Required | - |
| `body` | [`UpdatePreparedStatementInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/update-prepared-statement-input.md) | Body, Required | - |
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
const xAmzTarget = XAmzTarget58.EnumAmazonAthenaUpdatePreparedStatement;

const body: UpdatePreparedStatementInput = {
  statementName: 'StatementName4',
  workGroup: 'WorkGroup8',
  queryStatement: 'QueryStatement8',
};

try {
  const response = await api.updatePreparedStatement(
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
| 482 | ResourceNotFoundException | `ApiError` |



