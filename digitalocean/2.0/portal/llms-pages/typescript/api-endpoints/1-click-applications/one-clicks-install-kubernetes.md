# One Clicks Install Kubernetes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRjEtQ2xpY2slMjUyMEFwcGxpY2F0aW9ucyUyRm9uZUNsaWNrc19pbnN0YWxsX2t1YmVybmV0ZXM

To install a Kubernetes 1-Click application on a cluster, send a POST request to
`/v2/1-clicks/kubernetes`. The `addon_slugs` and `cluster_uuid` must be provided as body
parameter in order to specify which 1-Click application(s) to install. To list all available
1-Click Kubernetes applications, send a request to `/v2/1-clicks?type=kubernetes`.

```ts
async oneClicksInstallKubernetes(
  body: V21ClicksKubernetesRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V21ClicksKubernetesResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V21ClicksKubernetesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-1-clicks-kubernetes-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The response will verify that a job has been successfully created to install a 1-Click. The
post-installation lifecycle of a 1-Click application can not be managed via the DigitalOcean
API. For additional details specific to the 1-Click, find and view its
[DigitalOcean Marketplace](https://marketplace.digitalocean.com) page.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V21ClicksKubernetesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-1-clicks-kubernetes-response.md).


# Example Usage

```ts
const body: V21ClicksKubernetesRequest = {
  addonSlugs: [
    'kube-state-metrics',
    'loki'
  ],
  clusterUuid: '50a994b6-c303-438f-9495-7e896cfe6b08',
};

try {
  const response = await m1ClickApplicationsApi.oneClicksInstallKubernetes(body);

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
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
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
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



