# List Tags for Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRkxpc3RUYWdzRm9yUmVzb3VyY2U

Lists the tags associated with an Athena workgroup or data catalog resource.

```ts
async listTagsForResource(
  xAmzTarget: XAmzTarget44,
  body: ListTagsForResourceInput,
  xAmzContentSha256?: string,
  xAmzDate?: string,
  xAmzAlgorithm?: string,
  xAmzCredential?: string,
  xAmzSecurityToken?: string,
  xAmzSignature?: string,
  xAmzSignedHeaders?: string,
  maxResults?: string,
  nextToken?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ListTagsForResourceOutput>>
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/x-amz-target-44.md) | Header, Required | - |
| `body` | [`ListTagsForResourceInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/list-tags-for-resource-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string \| undefined` | Header, Optional | - |
| `xAmzDate` | `string \| undefined` | Header, Optional | - |
| `xAmzAlgorithm` | `string \| undefined` | Header, Optional | - |
| `xAmzCredential` | `string \| undefined` | Header, Optional | - |
| `xAmzSecurityToken` | `string \| undefined` | Header, Optional | - |
| `xAmzSignature` | `string \| undefined` | Header, Optional | - |
| `xAmzSignedHeaders` | `string \| undefined` | Header, Optional | - |
| `maxResults` | `string \| undefined` | Query, Optional | Pagination limit |
| `nextToken` | `string \| undefined` | Query, Optional | Pagination token |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ListTagsForResourceOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/list-tags-for-resource-output.md).


# Example Usage

```ts
const xAmzTarget = XAmzTarget44.EnumAmazonAthenaListTagsForResource;

const body: ListTagsForResourceInput = {
  resourceArn: 'ResourceARN4',
};

try {
  const response = await api.listTagsForResource(
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



