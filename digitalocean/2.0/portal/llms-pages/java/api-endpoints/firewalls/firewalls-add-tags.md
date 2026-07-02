# Firewalls Add Tags

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc19hZGRfdGFncw

To assign a tag representing a group of Droplets to a firewall, send a POST
request to `/v2/firewalls/$FIREWALL_ID/tags`. In the body of the request,
there should be a `tags` attribute containing a list of tag names.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.

```java
CompletableFuture<ApiResponse<Void>> firewallsAddTagsAsync(
    final UUID firewallId,
    final V2FirewallsTagsRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewallId` | `UUID` | Template, Required | A unique ID that can be used to identify and reference a firewall. |
| `body` | [`V2FirewallsTagsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-firewalls-tags-request.md) | Body, Optional | - |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
UUID firewallId = UUID.fromString("bb4b2611-3d72-467b-8602-280330ecd65c");
V2FirewallsTagsRequest body = new V2FirewallsTagsRequest.Builder(
    Arrays.asList(
        "frontend"
    )
)
.build();

firewallsApi.firewallsAddTagsAsync(firewallId, body).thenAccept(result -> {
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
| 400 | Bad Request | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



