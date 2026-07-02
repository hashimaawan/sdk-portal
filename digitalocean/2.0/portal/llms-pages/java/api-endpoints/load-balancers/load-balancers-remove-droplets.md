# Load Balancers Remove Droplets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfcmVtb3ZlX2Ryb3BsZXRz

To remove a Droplet from a load balancer instance, send a DELETE request to
`/v2/load_balancers/$LOAD_BALANCER_ID/droplets`. In the body of the request,
there should be a `droplet_ids` attribute containing a list of Droplet IDs.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.

```java
CompletableFuture<ApiResponse<Void>> loadBalancersRemoveDropletsAsync(
    final String lbId,
    final V2LoadBalancersDropletsRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lbId` | `String` | Template, Required | A unique identifier for a load balancer. |
| `body` | [`V2LoadBalancersDropletsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-load-balancers-droplets-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
String lbId = "4de7ac8b-495b-4884-9a69-1050c6793cd6";
V2LoadBalancersDropletsRequest body = new V2LoadBalancersDropletsRequest.Builder()
    .dropletIds(Arrays.asList(
        3164444,
        3164445
    ))
    .build();

loadBalancersApi.loadBalancersRemoveDropletsAsync(lbId, body).thenAccept(result -> {
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



