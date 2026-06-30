# Get Details of File by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0ZSUyRkZpbGVzJTJGR2V0RGV0YWlsc09mRmlsZUJ5SWQ

```java
CompletableFuture<ApiResponse<File>> getDetailsOfFileByIdAsync(
    final UUID vaultUuid,
    final UUID itemUuid,
    final UUID fileUuid,
    final Boolean inlineFiles)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `UUID` | Template, Required | The UUID of the Vault to fetch Item from |
| `itemUuid` | `UUID` | Template, Required | The UUID of the Item to fetch File from |
| `fileUuid` | `UUID` | Template, Required | The UUID of the File to fetch |
| `inlineFiles` | `Boolean` | Query, Optional | Tells server to return the base64-encoded file contents in the response. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`File`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/file.md).


# Example Usage

```java
UUID vaultUuid = UUID.fromString("00002186-0000-0000-0000-000000000000");
UUID itemUuid = UUID.fromString("0000141a-0000-0000-0000-000000000000");
UUID fileUuid = UUID.fromString("000008e0-0000-0000-0000-000000000000");
Boolean inlineFiles = true;

filesApi.getDetailsOfFileByIdAsync(vaultUuid, itemUuid, fileUuid, inlineFiles).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ErrorResponseException) {
        ErrorResponseException errorResponseException = (ErrorResponseException) cause;
        errorResponseException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/exceptions/error-response.md) |
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/exceptions/error-response.md) |
| 413 | File content too large to display | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/exceptions/error-response.md) |



