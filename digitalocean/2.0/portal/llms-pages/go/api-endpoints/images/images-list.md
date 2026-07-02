# Images List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkltYWdlcyUyRmltYWdlc19saXN0

To list all of the images available on your account, send a GET request to /v2/images.

## Filtering Results

-----


It's possible to request filtered results by including certain query parameters.

**Image Type**

Either 1-Click Application or OS Distribution images can be filtered by using the `type` query parameter.

> Important: The `type` query parameter does not directly relate to the `type` attribute.

To retrieve only ***distribution*** images, include the `type` query parameter set to distribution, `/v2/images?type=distribution`.

To retrieve only ***application*** images, include the `type` query parameter set to application, `/v2/images?type=application`.

**User Images**

To retrieve only the private images of a user, include the `private` query parameter set to true, `/v2/images?private=true`.

**Tags**

To list all images assigned to a specific tag, include the `tag_name` query parameter set to the name of the tag in your GET request. For example, `/v2/images?tag_name=$TAG_NAME`.

```go
ImagesList(
    ctx context.Context,
    mType *models.Type14,
    private *bool,
    tagName *string,
    perPage *int,
    page *int) (
    models.ApiResponse[models.V2ImagesResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mType` | [`*models.Type14`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-14.md) | Query, Optional | Filters results based on image type which can be either `application` or `distribution`. |
| `private` | `*bool` | Query, Optional | Used to filter only user images. |
| `tagName` | `*string` | Query, Optional | Used to filter images by a specific tag. |
| `perPage` | `*int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `*int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: The response will be a JSON object with a key called `images`.  This will be set to an array of image objects, each of which will contain the standard image attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2ImagesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-images-response.md).


# Example Usage

```go
ctx := context.Background()

mType := models.Type14_Distribution

private := true

tagName := "base-image"

perPage := 2

page := 1

apiResponse, err := imagesApi.ImagesList(ctx, &mType, &private, &tagName, &perPage, &page)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "images": [
    {
      "created_at": "2014-11-04T22:23:02Z",
      "description": "",
      "distribution": "Ubuntu",
      "error_message": "",
      "id": 7555620,
      "min_disk_size": 20,
      "name": "Nifty New Snapshot",
      "public": false,
      "regions": [
        "nyc2",
        "nyc3"
      ],
      "size_gigabytes": 2.34,
      "slug": null,
      "status": "available",
      "tags": [],
      "type": "snapshot"
    },
    {
      "created_at": "2014-11-04T22:23:02Z",
      "description": "",
      "distribution": "Ubuntu",
      "error_message": "",
      "id": 7555621,
      "min_disk_size": 20,
      "name": "Another Snapshot",
      "public": false,
      "regions": [
        "nyc2"
      ],
      "size_gigabytes": 2.34,
      "slug": null,
      "status": "available",
      "tags": [],
      "type": "snapshot"
    },
    {
      "created_at": "2020-05-15T05:47:50Z",
      "description": "",
      "distribution": "Ubuntu",
      "error_message": "",
      "id": 63663980,
      "min_disk_size": 20,
      "name": "20.04 (LTS) x64",
      "public": true,
      "regions": [
        "nyc2",
        "nyc3"
      ],
      "size_gigabytes": 2.36,
      "slug": "ubuntu-20-04-x64",
      "status": "available",
      "tags": [],
      "type": "snapshot"
    },
    {
      "created_at": "2014-11-04T22:23:02Z",
      "description": "",
      "distribution": "Arch Linux",
      "error_message": "",
      "id": 7555621,
      "min_disk_size": 20,
      "name": "A custom image",
      "public": false,
      "regions": [
        "nyc3"
      ],
      "size_gigabytes": 2.34,
      "slug": null,
      "status": "available",
      "tags": [],
      "type": "custom"
    },
    {
      "created_at": "2014-11-04T22:23:02Z",
      "description": "",
      "distribution": "Fedora",
      "error_message": "",
      "id": 7555621,
      "min_disk_size": 20,
      "name": "An APP image",
      "public": false,
      "regions": [
        "nyc2",
        "nyc3"
      ],
      "size_gigabytes": 2.34,
      "slug": null,
      "status": "available",
      "tags": [],
      "type": "snapshot"
    },
    {
      "created_at": "2014-11-04T22:23:02Z",
      "description": "",
      "distribution": "CentOS",
      "error_message": "",
      "id": 7555621,
      "min_disk_size": 20,
      "name": "A simple tagged image",
      "public": false,
      "regions": [
        "nyc2",
        "nyc3"
      ],
      "size_gigabytes": 2.34,
      "slug": null,
      "status": "available",
      "tags": [
        "simple-image"
      ],
      "type": "snapshot"
    }
  ],
  "links": {
    "pages": {}
  },
  "meta": {
    "total": 6
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



