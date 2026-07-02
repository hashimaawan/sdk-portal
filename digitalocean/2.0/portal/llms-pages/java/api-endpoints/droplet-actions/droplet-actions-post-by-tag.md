# Droplet Actions Post by Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRyb3BsZXQlMjUyMEFjdGlvbnMlMkZkcm9wbGV0QWN0aW9uc19wb3N0X2J5VGFn

Some actions can be performed in bulk on tagged Droplets. The actions can be
initiated by sending a POST to `/v2/droplets/actions?tag_name=$TAG_NAME` with
the action arguments.

Only a sub-set of action types are supported:

- `power_cycle`
- `power_on`
- `power_off`
- `shutdown`
- `enable_ipv6`
- `enable_backups`
- `disable_backups`
- `snapshot`

```java
CompletableFuture<ApiResponse<V2DropletsActionsResponse>> dropletActionsPostByTagAsync(
    final String tagName,
    final DropletActionsPostByTagBody body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tagName` | `String` | Query, Optional | Used to filter Droplets by a specific tag. Can not be combined with `name`. |
| `body` | [`DropletActionsPostByTagBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/droplet-actions-post-by-tag-body.md) | Body, Optional | This is a container for one-of cases. |


# Response Type

**201**: The response will be a JSON object with a key called `actions`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2DropletsActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-droplets-actions-response.md).


# Example Usage

```java
String tagName = "env:prod";
DropletActionsPostByTagBody body = DropletActionsPostByTagBody.fromV2DropletsActionsRequest(
    new V2DropletsActionsRequest.Builder(
        Type12.REBOOT
    )
    .build()
);

dropletActionsApi.dropletActionsPostByTagAsync(tagName, body).thenAccept(result -> {
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



