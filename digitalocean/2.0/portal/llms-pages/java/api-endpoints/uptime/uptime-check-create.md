# Uptime Check Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRlVwdGltZSUyRnVwdGltZV9jaGVja19jcmVhdGU

To create an Uptime check, send a POST request to `/v2/uptime/checks` specifying the attributes
in the table below in the JSON body.

```java
CompletableFuture<ApiResponse<V2UptimeChecksResponse1>> uptimeCheckCreateAsync(
    final V2UptimeChecksRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2UptimeChecksRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-uptime-checks-request.md) | Body, Required | - |


# Response Type

**201**: The response will be a JSON object with a key called `check`. The value of this will be an object that contains the standard attributes associated with an uptime check.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2UptimeChecksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-uptime-checks-response-1.md).


# Example Usage

```java
V2UptimeChecksRequest body = new V2UptimeChecksRequest.Builder()
    .enabled(true)
    .name("Landing page check")
    .regions(Arrays.asList(
        Region8.US_EAST,
        Region8.EU_WEST
    ))
    .target("https://www.landingpage.com")
    .type(Type19.HTTPS)
    .build();

uptimeApi.uptimeCheckCreateAsync(body).thenAccept(result -> {
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



