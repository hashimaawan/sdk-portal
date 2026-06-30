# Get Server Health

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldFNlcnZlckhlYWx0aA

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<HealthResponse>> getServerHealthAsync()
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`HealthResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/health-response.md).


# Example Usage

```java
healthApi.getServerHealthAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "dependencies": [
    {
      "service": "sync",
      "status": "TOKEN_NEEDED"
    },
    {
      "message": "Connected to./1password.sqlite",
      "service": "sqlite",
      "status": "ACTIVE"
    }
  ],
  "name": "1Password Connect API",
  "version": "1.2.1"
}
```



