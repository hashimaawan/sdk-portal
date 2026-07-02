# Kubernetes List Associated Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2xpc3RfYXNzb2NpYXRlZFJlc291cmNlcw

To list the associated billable resources that can be destroyed along with a cluster, send a GET request to the `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/destroy_with_associated_resources` endpoint.

```csharp
KubernetesListAssociatedResourcesAsync(
    Guid clusterId)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `Guid` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |


# Response Type

**200**: The response will be a JSON object containing `load_balancers`, `volumes`, and `volume_snapshots` keys. Each will be set to an array of objects containing the standard attributes for associated resources.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2KubernetesClustersDestroyWithAssociatedResourcesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-kubernetes-clusters-destroy-with-associated-resources-response.md).


# Example Usage

```csharp
Guid clusterId = new Guid("bd5f5959-5e1e-4205-a714-a914373942af");
try
{
    ApiResponse<V2KubernetesClustersDestroyWithAssociatedResourcesResponse> result = await kubernetesApi.KubernetesListAssociatedResourcesAsync(clusterId);
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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



