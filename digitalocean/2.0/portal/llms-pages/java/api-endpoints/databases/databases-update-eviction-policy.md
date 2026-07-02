# Databases Update Eviction Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc191cGRhdGVfZXZpY3Rpb25Qb2xpY3k

To configure an eviction policy for an existing Redis cluster, send a PUT request to `/v2/databases/$DATABASE_ID/eviction_policy` specifying the desired policy.

```java
CompletableFuture<ApiResponse<Void>> databasesUpdateEvictionPolicyAsync(
    final UUID databaseClusterUuid,
    final V2DatabasesEvictionPolicyRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `UUID` | Template, Required | A unique identifier for a database cluster. |
| `body` | [`V2DatabasesEvictionPolicyRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-databases-eviction-policy-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
UUID databaseClusterUuid = UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30");
V2DatabasesEvictionPolicyRequest body = new V2DatabasesEvictionPolicyRequest.Builder(
    RedisMaxmemoryPolicy.ALLKEYS_LRU
)
.build();

databasesApi.databasesUpdateEvictionPolicyAsync(databaseClusterUuid, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



