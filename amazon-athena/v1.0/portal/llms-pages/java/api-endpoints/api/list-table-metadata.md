# List Table Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRkxpc3RUYWJsZU1ldGFkYXRh

Lists the metadata for the tables in the specified data catalog database.

```java
CompletableFuture<ListTableMetadataOutput> listTableMetadataAsync(
    final XAmzTarget43Enum xAmzTarget,
    final ListTableMetadataInput body,
    final String xAmzContentSha256,
    final String xAmzDate,
    final String xAmzAlgorithm,
    final String xAmzCredential,
    final String xAmzSecurityToken,
    final String xAmzSignature,
    final String xAmzSignedHeaders,
    final String maxResults,
    final String nextToken)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget43Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/x-amz-target-43.md) | Header, Required | - |
| `body` | [`ListTableMetadataInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-table-metadata-input.md) | Body, Required | - |
| `xAmzContentSha256` | `String` | Header, Optional | - |
| `xAmzDate` | `String` | Header, Optional | - |
| `xAmzAlgorithm` | `String` | Header, Optional | - |
| `xAmzCredential` | `String` | Header, Optional | - |
| `xAmzSecurityToken` | `String` | Header, Optional | - |
| `xAmzSignature` | `String` | Header, Optional | - |
| `xAmzSignedHeaders` | `String` | Header, Optional | - |
| `maxResults` | `String` | Query, Optional | Pagination limit |
| `nextToken` | `String` | Query, Optional | Pagination token |


# Response Type

**200**: Success

[`ListTableMetadataOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/list-table-metadata-output.md)


# Example Usage

```java
XAmzTarget43Enum xAmzTarget = XAmzTarget43Enum.ENUM_AMAZONATHENALISTTABLEMETADATA;
ListTableMetadataInput body = new ListTableMetadataInput.Builder(
    "CatalogName0",
    "DatabaseName0"
)
.build();


aPIController.listTableMetadataAsync(xAmzTarget, body, null, null, null, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |
| 482 | MetadataException | `ApiException` |



