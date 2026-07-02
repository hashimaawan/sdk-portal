# One Clicks Install Kubernetes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRjEtQ2xpY2slMjUyMEFwcGxpY2F0aW9ucyUyRm9uZUNsaWNrc19pbnN0YWxsX2t1YmVybmV0ZXM

To install a Kubernetes 1-Click application on a cluster, send a POST request to
`/v2/1-clicks/kubernetes`. The `addon_slugs` and `cluster_uuid` must be provided as body
parameter in order to specify which 1-Click application(s) to install. To list all available
1-Click Kubernetes applications, send a request to `/v2/1-clicks?type=kubernetes`.

```csharp
OneClicksInstallKubernetesAsync(
    Models.V21ClicksKubernetesRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V21ClicksKubernetesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-1-clicks-kubernetes-request.md) | Body, Required | - |


# Response Type

**200**: The response will verify that a job has been successfully created to install a 1-Click. The
post-installation lifecycle of a 1-Click application can not be managed via the DigitalOcean
API. For additional details specific to the 1-Click, find and view its
[DigitalOcean Marketplace](https://marketplace.digitalocean.com) page.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V21ClicksKubernetesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-1-clicks-kubernetes-response.md).


# Example Usage

```csharp
V21ClicksKubernetesRequest body = new V21ClicksKubernetesRequest
{
    AddonSlugs = new List<string>
    {
        "kube-state-metrics",
        "loki",
    },
    ClusterUuid = "50a994b6-c303-438f-9495-7e896cfe6b08",
};

try
{
    ApiResponse<V21ClicksKubernetesResponse> result = await m1ClickApplicationsApi.OneClicksInstallKubernetesAsync(body);
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
  "message": "Successfully kicked off addon job."
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



