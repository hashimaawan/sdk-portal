# Kubernetes Get Cluster Lint Results

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2dldF9jbHVzdGVyTGludFJlc3VsdHM

To request clusterlint diagnostics for your cluster, send a GET request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/clusterlint`. If the `run_id` query
parameter is provided, then the diagnostics for the specific run is fetched.
By default, the latest results are shown.

To find out how to address clusterlint feedback, please refer to
[the clusterlint check documentation](https://github.com/digitalocean/clusterlint/blob/master/checks.md).

```ts
async kubernetesGetClusterLintResults(
  clusterId: string,
  runId?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2KubernetesClustersClusterlintResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `string` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `runId` | `string \| undefined` | Query, Optional | Specifies the clusterlint run whose results will be retrieved. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The response is a JSON object which contains the diagnostics on Kubernetes
objects in the cluster. Each diagnostic will contain some metadata information
about the object and feedback for users to act upon.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2KubernetesClustersClusterlintResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-kubernetes-clusters-clusterlint-response.md).


# Example Usage

```ts
const clusterId = 'bd5f5959-5e1e-4205-a714-a914373942af';

const runId = '50c2f44c-011d-493e-aee5-361a4a0d1844';

try {
  const response = await kubernetesApi.kubernetesGetClusterLintResults(
    clusterId,
    runId
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



