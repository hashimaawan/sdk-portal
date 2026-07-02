# Tag Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlRhZ1Jlc291cmNl

Adds one or more tags to an Athena resource. A tag is a label that you assign to a resource. In Athena, a resource can be a workgroup or data catalog. Each tag consists of a key and an optional value, both of which you define. For example, you can use tags to categorize Athena workgroups or data catalogs by purpose, owner, or environment. Use a consistent set of tag keys to make it easier to search and filter workgroups or data catalogs in your account. For best practices, see <a href="https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/tagging-best-practices.html">Tagging Best Practices</a>. Tag keys can be from 1 to 128 UTF-8 Unicode characters, and tag values can be from 0 to 256 UTF-8 Unicode characters. Tags can use letters and numbers representable in UTF-8, and the following characters: + - = . _ : / @. Tag keys and values are case-sensitive. Tag keys must be unique per resource. If you specify more than one tag, separate them by commas.

```ts
async tagResource(
  xAmzTarget: XAmzTarget51,
  body: TagResourceInput,
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
| `xAmzTarget` | [`XAmzTarget51`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/x-amz-target-51.md) | Header, Required | - |
| `body` | [`TagResourceInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/tag-resource-input.md) | Body, Required | - |
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
const xAmzTarget = XAmzTarget51.EnumAmazonAthenaTagResource;

const body: TagResourceInput = {
  resourceArn: 'ResourceARN4',
  tags: [
    {
    }
  ],
};

try {
  const response = await api.tagResource(
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



