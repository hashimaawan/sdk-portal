# Reserved I Ps Actions Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRlJlc2VydmVkJTI1MjBJUCUyNTIwQWN0aW9ucyUyRnJlc2VydmVkSVBzQWN0aW9uc19wb3N0

To initiate an action on a reserved IP send a POST request to
`/v2/reserved_ips/$RESERVED_IP/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action     | Details
|------------|--------
| `assign`   | Assigns a reserved IP to a Droplet
| `unassign` | Unassign a reserved IP from a Droplet

```java
CompletableFuture<ApiResponse<V2ReservedIpsActionsResponse1>> reservedIPsActionsPostAsync(
    final String reservedIp,
    final ReservedIPsActionsPostBody body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reservedIp` | `String` | Template, Required | A reserved IP address. |
| `body` | [`ReservedIPsActionsPostBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/reserved-i-ps-actions-post-body.md) | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard reserved IP action attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2ReservedIpsActionsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-reserved-ips-actions-response-1.md).


# Example Usage

```java
String reservedIp = "45.55.96.47";
ReservedIPsActionsPostBody body = ReservedIPsActionsPostBody.fromBaseType(
    new V2ReservedIpsActionsRequest.Builder(
        758604968
    )
    .type("V2 Reserved Ips Actions Request")
    .build()
);

reservedIpActionsApi.reservedIPsActionsPostAsync(reservedIp, body).thenAccept(result -> {
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



