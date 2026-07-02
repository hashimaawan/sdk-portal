# Droplet Actions Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRyb3BsZXQlMjUyMEFjdGlvbnMlMkZkcm9wbGV0QWN0aW9uc19wb3N0

To initiate an action on a Droplet send a POST request to
`/v2/droplets/$DROPLET_ID/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action                                   | Details |
| ---------------------------------------- | ----------- |
| <nobr>`enable_backups`</nobr>            | Enables backups for a Droplet |
| <nobr>`disable_backups`</nobr>           | Disables backups for a Droplet |
| <nobr>`reboot`</nobr>                    | Reboots a Droplet. A `reboot` action is an attempt to reboot the Droplet in a graceful way, similar to using the `reboot` command from the console. |
| <nobr>`power_cycle`</nobr>               | Power cycles a Droplet. A `powercycle` action is similar to pushing the reset button on a physical machine, it's similar to booting from scratch. |
| <nobr>`shutdown`</nobr>                  | Shutsdown a Droplet. A shutdown action is an attempt to shutdown the Droplet in a graceful way, similar to using the `shutdown` command from the console. Since a `shutdown` command can fail, this action guarantees that the command is issued, not that it succeeds. The preferred way to turn off a Droplet is to attempt a shutdown, with a reasonable timeout, followed by a `power_off` action to ensure the Droplet is off. |
| <nobr>`power_off`</nobr>                 | Powers off a Droplet. A `power_off` event is a hard shutdown and should only be used if the `shutdown` action is not successful. It is similar to cutting the power on a server and could lead to complications. |
| <nobr>`power_on`</nobr>                  | Powers on a Droplet. |
| <nobr>`restore`</nobr>                   | Restore a Droplet using a backup image. The image ID that is passed in must be a backup of the current Droplet instance. The operation will leave any embedded SSH keys intact. |
| <nobr>`password_reset`</nobr>            | Resets the root password for a Droplet. A new password will be provided via email. It must be changed after first use. |
| <nobr>`resize`</nobr>                    | Resizes a Droplet. Set the `size` attribute to a size slug. If a permanent resize with disk changes included is desired, set the `disk` attribute to `true`. |
| <nobr>`rebuild`</nobr>                   | Rebuilds a Droplet from a new base image. Set the `image` attribute to an image ID or slug. |
| <nobr>`rename`</nobr>                    | Renames a Droplet. |
| <nobr>`change_kernel`</nobr>             | Changes a Droplet's kernel. Only applies to Droplets with externally managed kernels. All Droplets created after March 2017 use internal kernels by default. |
| <nobr>`enable_ipv6`</nobr>               | Enables IPv6 for a Droplet. |
| <nobr>`snapshot`</nobr>                  | Takes a snapshot of a Droplet. |

```go
DropletActionsPost(
    ctx context.Context,
    dropletId int,
    body *models.DropletActionsPostBody) (
    models.ApiResponse[models.V2DropletsActionsResponse2],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `body` | [`*models.DropletActionsPostBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/droplet-actions-post-body.md) | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response will be a JSON object with a key called `action`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2DropletsActionsResponse2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-actions-response-2.md).


# Example Usage

```go
ctx := context.Background()

dropletId := 3164444

body := models.DropletActionsPostBodyContainer.FromV2DropletsActionsRequest(models.V2DropletsActionsRequest{
    Type:                  models.Type12_Reboot,
})

apiResponse, err := dropletActionsApi.DropletActionsPost(ctx, dropletId, &body)
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
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



