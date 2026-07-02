# Tags Unassign Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRlRhZ3MlMkZ0YWdzX3VuYXNzaWduX3Jlc291cmNlcw

Resources can be untagged by sending a DELETE request to `/v2/tags/$TAG_NAME/resources` with an array of json objects containing `resource_id` and `resource_type` attributes.
Currently only untagging of Droplets, Databases, Images, Volumes, and Volume Snapshots is supported. `resource_type` is expected to be the string `droplet`, `database`, `image`, `volume` or `volume_snapshot`. `resource_id` is expected to be the ID of the resource as a string.

```java
CompletableFuture<ApiResponse<Void>> tagsUnassignResourcesAsync(
    final String tagId,
    final V2TagsResourcesRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tagId` | `String` | Template, Required | The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores. There is a limit of 255 characters per tag.<br><br>**Constraints**: *Maximum Length*: `255`, *Pattern*: `^[a-zA-Z0-9_\-\:]+$` |
| `body` | [`V2TagsResourcesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-tags-resources-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
String tagId = "awesome";
V2TagsResourcesRequest body = new V2TagsResourcesRequest.Builder(
    Arrays.asList(
        new Resources3.Builder()
            .resourceId("9569411")
            .resourceType(ResourceType2.DROPLET)
            .build(),
        new Resources3.Builder()
            .resourceId("7555620")
            .resourceType(ResourceType2.IMAGE)
            .build(),
        new Resources3.Builder()
            .resourceId("3d80cb72-342b-4aaa-b92e-4e4abb24a933")
            .resourceType(ResourceType2.VOLUME)
            .build()
    )
)
.build();

tagsApi.tagsUnassignResourcesAsync(tagId, body).thenAccept(result -> {
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



