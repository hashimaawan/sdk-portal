# Update an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0ZSUyRkltYWdlcyUyRlVwZGF0ZSUyNTIwYW4lMjUyMEltYWdl

Updates the Image. You may change the description, convert a Backup Image to a Snapshot Image or change the Image labels. Only Images of type `snapshot` and `backup` can be updated.

Note that when updating labels, the current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateAnImage(
  id: number,
  body?: UpdateImageRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ImagesResponse1>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Image |
| `body` | [`UpdateImageRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/update-image-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The image key in the reply contains the modified Image object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ImagesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/images-response-1.md).


# Example Usage

```ts
const id = 112;

const body: UpdateImageRequest = {
  description: 'My new Image description',
  labels: { 'labelkey': 'value' },
};

try {
  const response = await imagesController.updateAnImage(
    id,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# Example Response *(as JSON)*

```json
{
  "image": {
    "bound_to": null,
    "build_id": "c313fe40383af26094a5a92026054320ab55abc7",
    "created": "2016-01-30T23:50:00+00:00",
    "created_from": {
      "id": 1,
      "name": "Server"
    },
    "deleted": null,
    "deprecated": "2018-02-28T00:00:00+00:00",
    "description": "My new Image description",
    "disk_size": 10,
    "id": 4711,
    "image_size": 2.3,
    "labels": {
      "labelkey": "value"
    },
    "name": null,
    "os_flavor": "ubuntu",
    "os_version": "20.04",
    "protection": {
      "delete": false
    },
    "rapid_deploy": false,
    "status": "available",
    "type": "snapshot"
  }
}
```



