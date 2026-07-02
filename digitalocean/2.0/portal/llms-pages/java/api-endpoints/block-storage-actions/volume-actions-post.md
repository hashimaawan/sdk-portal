# Volume Actions Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkJsb2NrJTI1MjBTdG9yYWdlJTI1MjBBY3Rpb25zJTJGdm9sdW1lQWN0aW9uc19wb3N0

To initiate an action on a block storage volume by Name, send a POST request to
`~/v2/volumes/actions`. The body should contain the appropriate
attributes for the respective action.

## Attach a Block Storage Volume to a Droplet

| Attribute   | Details                                                             |
| ----------- | ------------------------------------------------------------------- |
| type        | This must be `attach`                                               |
| volume_name | The name of the block storage volume                                |
| droplet_id  | Set to the Droplet's ID                                             |
| region      | Set to the slug representing the region where the volume is located |

Each volume may only be attached to a single Droplet. However, up to five
volumes may be attached to a Droplet at a time. Pre-formatted volumes will be
automatically mounted to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS
Droplets created on or after April 26, 2018 when attached. On older Droplets,
[additional configuration](https://www.digitalocean.com/community/tutorials/how-to-partition-and-format-digitalocean-block-storage-volumes-in-linux#mounting-the-filesystems)
is required.

## Remove a Block Storage Volume from a Droplet

| Attribute   | Details                                                             |
| ----------- | ------------------------------------------------------------------- |
| type        | This must be `detach`                                               |
| volume_name | The name of the block storage volume                                |
| droplet_id  | Set to the Droplet's ID                                             |
| region      | Set to the slug representing the region where the volume is located |

```java
CompletableFuture<ApiResponse<V2VolumesActionsResponse>> volumeActionsPostAsync(
    final VolumeActionsPostBody body,
    final Integer perPage,
    final Integer page)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`VolumeActionsPostBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/volume-actions-post-body.md) | Body, Required | This is a container for any-of cases. |
| `perPage` | `Integer` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `Integer` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**202**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard volume action attributes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2VolumesActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-volumes-actions-response.md).


# Example Usage

```java
VolumeActionsPostBody body = VolumeActionsPostBody.fromV2VolumesActionsRequest(
    new V2VolumesActionsRequest.Builder(
        Type21.ATTACH,
        11612190
    )
    .region(Region2.NYC1)
    .tags(Arrays.asList(
            "aninterestingtag"
        ))
    .additionalProperty("volume_name", ApiHelper.deserialize("\"example\""))
    .build()
);

blockStorageActionsApi.volumeActionsPostAsync(body, null, null).thenAccept(result -> {
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


# Example Response *(as JSON)*

```json
{
  "action": {
    "completed_at": null,
    "id": 68212773,
    "region": {
      "available": true,
      "features": [
        "private_networking",
        "backups",
        "ipv6",
        "metadata"
      ],
      "name": "New York 1",
      "sizes": [
        "s-1vcpu-1gb",
        "s-1vcpu-2gb",
        "s-1vcpu-3gb",
        "s-2vcpu-2gb",
        "s-3vcpu-1gb",
        "s-2vcpu-4gb",
        "s-4vcpu-8gb",
        "s-6vcpu-16gb",
        "s-8vcpu-32gb",
        "s-12vcpu-48gb",
        "s-16vcpu-64gb",
        "s-20vcpu-96gb",
        "s-24vcpu-128gb",
        "s-32vcpu-192gb"
      ],
      "slug": "nyc1"
    },
    "region_slug": "nyc1",
    "resource_id": null,
    "resource_type": "backend",
    "started_at": "2015-10-15T17:46:15Z",
    "status": "in-progress",
    "type": "detach_volume"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



