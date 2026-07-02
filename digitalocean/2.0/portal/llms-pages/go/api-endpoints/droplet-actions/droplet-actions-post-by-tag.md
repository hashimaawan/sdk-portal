# Droplet Actions Post by Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRyb3BsZXQlMjUyMEFjdGlvbnMlMkZkcm9wbGV0QWN0aW9uc19wb3N0X2J5VGFn

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

```go
DropletActionsPostByTag(
    ctx context.Context,
    tagName *string,
    body *models.DropletActionsPostByTagBody) (
    models.ApiResponse[models.V2DropletsActionsResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tagName` | `*string` | Query, Optional | Used to filter Droplets by a specific tag. Can not be combined with `name`. |
| `body` | [`*models.DropletActionsPostByTagBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/droplet-actions-post-by-tag-body.md) | Body, Optional | This is a container for one-of cases. |


# Response Type

**201**: The response will be a JSON object with a key called `actions`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2DropletsActionsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-response.md).


# Example Usage

```go
ctx := context.Background()

tagName := "env:prod"

body := models.DropletActionsPostByTagBodyContainer.FromV2DropletsActionsRequest(models.V2DropletsActionsRequest{
    Type:                  models.Type12_Reboot,
})

apiResponse, err := dropletActionsApi.DropletActionsPostByTag(ctx, &tagName, &body)
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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



