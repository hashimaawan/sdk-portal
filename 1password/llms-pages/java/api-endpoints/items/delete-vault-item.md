# Delete Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0ZSUyRkl0ZW1zJTJGRGVsZXRlVmF1bHRJdGVt

```java
CompletableFuture<ApiResponse<Void>> deleteVaultItemAsync(
    final String vaultUuid,
    final String itemUuid)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `String` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `String` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |


# Response Type

**204**: Successfully deleted an item

`void`


# Example Usage

```java
String vaultUuid = "vaultUuid2";
String itemUuid = "itemUuid6";

itemsApi.deleteVaultItemAsync(vaultUuid, itemUuid).thenAccept(result -> {
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
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/exceptions/error-response.md) |



