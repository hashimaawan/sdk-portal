# Kubernetes Get Credentials

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2dldF9jcmVkZW50aWFscw

This endpoint returns a JSON object . It can be used to programmatically
construct Kubernetes clients which cannot parse kubeconfig files.

The resulting JSON object contains token-based authentication for clusters
supporting it, and certificate-based authentication otherwise. For a list of
supported versions and more information, see "[How to Connect to a DigitalOcean
Kubernetes Cluster with kubectl](https://www.digitalocean.com/docs/kubernetes/how-to/connect-with-kubectl/)".

To retrieve credentials for accessing a Kubernetes cluster, send a GET
request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/credentials`.

Clusters supporting token-based authentication may define an expiration by
passing a duration in seconds as a query parameter to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/kubeconfig?expiry_seconds=$DURATION_IN_SECONDS`.
If not set or 0, then the token will have a 7 day expiry. The query parameter
has no impact in certificate-based authentication.

```csharp
KubernetesGetCredentialsAsync(
    Guid clusterId,
    int? expirySeconds = 0)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `Guid` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `expirySeconds` | `int?` | Query, Optional | The duration in seconds that the returned Kubernetes credentials will be valid. If not set or 0, the credentials will have a 7 day expiry.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |


# Response Type

**200**: A JSON object containing credentials for a cluster.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2KubernetesClustersCredentialsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-kubernetes-clusters-credentials-response.md).


# Example Usage

```csharp
Guid clusterId = new Guid("bd5f5959-5e1e-4205-a714-a914373942af");
int? expirySeconds = 300;
try
{
    ApiResponse<V2KubernetesClustersCredentialsResponse> result = await kubernetesApi.KubernetesGetCredentialsAsync(
        clusterId,
        expirySeconds
    );
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



