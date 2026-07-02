# Image Actions Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkltYWdlJTI1MjBBY3Rpb25zJTJGaW1hZ2VBY3Rpb25zX3Bvc3Q

The following actions are available on an Image.

## Convert an Image to a Snapshot

To convert an image, for example, a backup to a snapshot, send a POST request
to `/v2/images/$IMAGE_ID/actions`. Set the `type` attribute to `convert`.

## Transfer an Image

To transfer an image to another region, send a POST request to
`/v2/images/$IMAGE_ID/actions`. Set the `type` attribute to `transfer` and set
`region` attribute to the slug identifier of the region you wish to transfer
to.

```csharp
ImageActionsPostAsync(
    int imageId,
    ImageActionsPostBody body = null)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `imageId` | `int` | Template, Required | A unique number that can be used to identify and reference a specific image. |
| `body` | [`ImageActionsPostBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/image-actions-post-body.md) | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response will be a JSON object with a key called `action`. The value of this will be an object containing the standard image action attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.Action](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/action.md).


# Example Usage

```csharp
int imageId = 62137902;
ImageActionsPostBody body = ImageActionsPostBody.FromV2ImagesActionsRequest(
    new V2ImagesActionsRequest
    {
        Type = Type15.Convert,
    }
);

try
{
    ApiResponse<Action> result = await imageActionsApi.ImageActionsPostAsync(
        imageId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "completed_at": null,
    "id": 36805527,
    "region": {
      "available": true,
      "features": [
        "private_networking",
        "backups",
        "ipv6",
        "metadata",
        "server_id",
        "install_agent",
        "storage",
        "image_transfer"
      ],
      "name": "New York 3",
      "sizes": [
        "s-1vcpu-3gb",
        "m-1vcpu-8gb",
        "s-3vcpu-1gb",
        "s-1vcpu-2gb",
        "s-2vcpu-2gb",
        "s-2vcpu-4gb",
        "s-4vcpu-8gb",
        "s-6vcpu-16gb",
        "s-8vcpu-32gb",
        "s-12vcpu-48gb",
        "s-16vcpu-64gb",
        "s-20vcpu-96gb",
        "s-1vcpu-1gb",
        "c-1vcpu-2gb",
        "s-24vcpu-128gb"
      ],
      "slug": "nyc3"
    },
    "region_slug": "nyc3",
    "resource_id": 7938269,
    "resource_type": "image",
    "started_at": "2014-11-14T16:42:45Z",
    "status": "in-progress",
    "type": "transfer"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



