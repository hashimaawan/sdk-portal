# Kubernetes Destroy Associated Resources Selective

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2Rlc3Ryb3lfYXNzb2NpYXRlZFJlc291cmNlc1NlbGVjdGl2ZQ

To delete a Kubernetes cluster along with a subset of its associated resources,
send a DELETE request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/destroy_with_associated_resources/selective`.

The JSON body of the request should include `load_balancers`, `volumes`, or
`volume_snapshots` keys each set to an array of IDs for the associated
resources to be destroyed.

The IDs can be found by querying the cluster's associated resources endpoint.
Any associated resource not included in the request will remain and continue
to accrue changes on your account.

```ts
async kubernetesDestroyAssociatedResourcesSelective(
  clusterId: string,
  body: V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `string` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-kubernetes-clusters-destroy-with-associated-resources-selective-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**204**: The action was successful and the response body is empty.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const clusterId = 'bd5f5959-5e1e-4205-a714-a914373942af';

const body: V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest = {
  loadBalancers: [
    '4de7ac8b-495b-4884-9a69-1050c6793cd6'
  ],
  volumeSnapshots: [
    'edb0478d-7436-11ea-86e6-0a58ac144b91'
  ],
  volumes: [
    'ba49449a-7435-11ea-b89e-0a58ac14480f'
  ],
};

try {
  const response = await kubernetesApi.kubernetesDestroyAssociatedResourcesSelective(
    clusterId,
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



