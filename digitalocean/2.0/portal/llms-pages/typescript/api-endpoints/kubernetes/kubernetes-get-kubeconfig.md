# Kubernetes Get Kubeconfig

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2dldF9rdWJlY29uZmln

This endpoint returns a kubeconfig file in YAML format. It can be used to
connect to and administer the cluster using the Kubernetes command line tool,
`kubectl`, or other programs supporting kubeconfig files (e.g., client libraries).

The resulting kubeconfig file uses token-based authentication for clusters
supporting it, and certificate-based authentication otherwise. For a list of
supported versions and more information, see "[How to Connect to a DigitalOcean
Kubernetes Cluster with kubectl](https://www.digitalocean.com/docs/kubernetes/how-to/connect-with-kubectl/)".

To retrieve a kubeconfig file for use with a Kubernetes cluster, send a GET
request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/kubeconfig`.

Clusters supporting token-based authentication may define an expiration by
passing a duration in seconds as a query parameter to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/kubeconfig?expiry_seconds=$DURATION_IN_SECONDS`.
If not set or 0, then the token will have a 7 day expiry. The query parameter
has no impact in certificate-based authentication.

```ts
async kubernetesGetKubeconfig(
  clusterId: string,
  expirySeconds?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<unknown>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `string` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `expirySeconds` | `number \| undefined` | Query, Optional | The duration in seconds that the returned Kubernetes credentials will be valid. If not set or 0, the credentials will have a 7 day expiry.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A kubeconfig file for the cluster in YAML format.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type `unknown`.


# Example Usage

```ts
const clusterId = 'bd5f5959-5e1e-4205-a714-a914373942af';

const expirySeconds = 300;

try {
  const response = await kubernetesApi.kubernetesGetKubeconfig(
    clusterId,
    expirySeconds
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
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



