# Droplets Destroy with Associated Resources Selective

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfZGVzdHJveV93aXRoQXNzb2NpYXRlZFJlc291cmNlc1NlbGVjdGl2ZQ

To destroy a Droplet along with a sub-set of its associated resources, send a
DELETE request to the `/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/selective`
endpoint. The JSON body of the request should include `reserved_ips`, `snapshots`, `volumes`,
or `volume_snapshots` keys each set to an array of IDs for the associated
resources to be destroyed. The IDs can be found by querying the Droplet's
associated resources. Any associated resource not included in the request
will remain and continue to accrue changes on your account.

A successful response will include a 202 response code and no content. Use
the status endpoint to check on the success or failure of the destruction of
the individual resources.

```java
CompletableFuture<ApiResponse<Void>> dropletsDestroyWithAssociatedResourcesSelectiveAsync(
    final int dropletId,
    final V2DropletsDestroyWithAssociatedResourcesSelectiveRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `body` | [`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-destroy-with-associated-resources-selective-request.md) | Body, Optional | - |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

`void`


# Example Usage

```java
int dropletId = 3164444;
V2DropletsDestroyWithAssociatedResourcesSelectiveRequest body = new V2DropletsDestroyWithAssociatedResourcesSelectiveRequest.Builder()
    .floatingIps(Arrays.asList(
        "6186916"
    ))
    .reservedIps(Arrays.asList(
        "6186916"
    ))
    .snapshots(Arrays.asList(
        "61486916"
    ))
    .volumeSnapshots(Arrays.asList(
        "edb0478d-7436-11ea-86e6-0a58ac144b91"
    ))
    .volumes(Arrays.asList(
        "ba49449a-7435-11ea-b89e-0a58ac14480f"
    ))
    .build();

dropletsApi.dropletsDestroyWithAssociatedResourcesSelectiveAsync(dropletId, body).thenAccept(result -> {
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



