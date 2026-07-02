# One Clicks Install Kubernetes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRjEtQ2xpY2slMjUyMEFwcGxpY2F0aW9ucyUyRm9uZUNsaWNrc19pbnN0YWxsX2t1YmVybmV0ZXM

To install a Kubernetes 1-Click application on a cluster, send a POST request to
`/v2/1-clicks/kubernetes`. The `addon_slugs` and `cluster_uuid` must be provided as body
parameter in order to specify which 1-Click application(s) to install. To list all available
1-Click Kubernetes applications, send a request to `/v2/1-clicks?type=kubernetes`.

```go
OneClicksInstallKubernetes(
    ctx context.Context,
    body models.V21ClicksKubernetesRequest) (
    models.ApiResponse[models.V21ClicksKubernetesResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`models.V21ClicksKubernetesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-1-clicks-kubernetes-request.md) | Body, Required | - |


# Response Type

**200**: The response will verify that a job has been successfully created to install a 1-Click. The
post-installation lifecycle of a 1-Click application can not be managed via the DigitalOcean
API. For additional details specific to the 1-Click, find and view its
[DigitalOcean Marketplace](https://marketplace.digitalocean.com) page.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V21ClicksKubernetesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-1-clicks-kubernetes-response.md).


# Example Usage

```go
ctx := context.Background()

body := models.V21ClicksKubernetesRequest{
    AddonSlugs:            []string{
        "kube-state-metrics",
        "loki",
    },
    ClusterUuid:           "50a994b6-c303-438f-9495-7e896cfe6b08",
}

apiResponse, err := m1ClickApplicationsApi.OneClicksInstallKubernetes(ctx, body)
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
  "message": "Successfully kicked off addon job."
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



