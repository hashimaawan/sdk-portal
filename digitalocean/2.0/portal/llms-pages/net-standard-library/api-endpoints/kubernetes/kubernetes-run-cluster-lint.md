# Kubernetes Run Cluster Lint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3J1bl9jbHVzdGVyTGludA

Clusterlint helps operators conform to Kubernetes best practices around
resources, security and reliability to avoid common problems while operating
or upgrading the clusters.

To request a clusterlint run on your cluster, send a POST request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/clusterlint`. This will run all
checks present in the `doks` group by default, if a request body is not
specified. Optionally specify the below attributes.

For information about the available checks, please refer to
[the clusterlint check documentation](https://github.com/digitalocean/clusterlint/blob/master/checks.md).

```csharp
KubernetesRunClusterLintAsync(
    Guid clusterId,
    Models.V2KubernetesClustersClusterlintRequest body = null)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `Guid` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`V2KubernetesClustersClusterlintRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-kubernetes-clusters-clusterlint-request.md) | Body, Optional | - |


# Response Type

**202**: The response is a JSON object with a key called `run_id` that you can later use to fetch the run results.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2KubernetesClustersClusterlintResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-kubernetes-clusters-clusterlint-response-1.md).


# Example Usage

```csharp
Guid clusterId = new Guid("bd5f5959-5e1e-4205-a714-a914373942af");
V2KubernetesClustersClusterlintRequest body = new V2KubernetesClustersClusterlintRequest
{
    ExcludeChecks = new List<string>
    {
        "default-namespace",
    },
    ExcludeGroups = new List<string>
    {
        "workload-health",
    },
    IncludeChecks = new List<string>
    {
        "bare-pods",
        "resource-requirements",
    },
    IncludeGroups = new List<string>
    {
        "basic",
        "doks",
        "security",
    },
};

try
{
    ApiResponse<V2KubernetesClustersClusterlintResponse1> result = await kubernetesApi.KubernetesRunClusterLintAsync(
        clusterId,
        body
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



