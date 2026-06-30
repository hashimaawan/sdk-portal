# Download File by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0ZSUyRkZpbGVzJTJGRG93bmxvYWRGaWxlQnlJRA

```java
CompletableFuture<ApiResponse<InputStream>> downloadFileByIdAsync(
    final UUID vaultUuid,
    final UUID itemUuid,
    final String fileUuid)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `UUID` | Template, Required | The UUID of the Vault the item is in |
| `itemUuid` | `UUID` | Template, Required | The UUID of the Item the File is in |
| `fileUuid` | `String` | Template, Required | UUID of the file to get content from |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type `InputStream`.


# Example Usage

```java
UUID vaultUuid = UUID.fromString("00002186-0000-0000-0000-000000000000");
UUID itemUuid = UUID.fromString("0000141a-0000-0000-0000-000000000000");
String fileUuid = "fileUuid2";

filesApi.downloadFileByIdAsync(vaultUuid, itemUuid, fileUuid).thenAccept(result -> {
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
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/exceptions/error-response.md) |



