# Patch Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0ZSUyRkl0ZW1zJTJGUGF0Y2hWYXVsdEl0ZW0

Applies a modified [RFC6902 JSON Patch](https://tools.ietf.org/html/rfc6902) document to an Item or ItemField. This endpoint only supports `add`, `remove` and `replace` operations.

When modifying a specific ItemField, the ItemField's ID in the `path` attribute of the operation object: `/fields/{fieldId}`

```java
CompletableFuture<ApiResponse<FullItem>> patchVaultItemAsync(
    final String vaultUuid,
    final String itemUuid,
    final List<Patch> body)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `String` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `String` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`List<Patch>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/patch.md) | Body, Optional | - |


# Response Type

**200**: OK - Item updated. If no Patch operations were provided, Item is unmodified.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/full-item.md).


# Example Usage

```java
String vaultUuid = "vaultUuid2";
String itemUuid = "itemUuid6";
List<Patch> body = Arrays.asList(
    new Patch.Builder(
        Op.ADD,
        "/fields"
    )
    .value(ApiHelper.deserialize("{\"label\":\"New Field\",\"type\":\"string\",\"value\":\"hunter2\"}"))
    .build()
);

itemsApi.patchVaultItemAsync(vaultUuid, itemUuid, body).thenAccept(result -> {
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



