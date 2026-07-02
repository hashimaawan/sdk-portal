# Kubernetes Run Cluster Lint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3J1bl9jbHVzdGVyTGludA

Clusterlint helps operators conform to Kubernetes best practices around
resources, security and reliability to avoid common problems while operating
or upgrading the clusters.

To request a clusterlint run on your cluster, send a POST request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/clusterlint`. This will run all
checks present in the `doks` group by default, if a request body is not
specified. Optionally specify the below attributes.

For information about the available checks, please refer to
[the clusterlint check documentation](https://github.com/digitalocean/clusterlint/blob/master/checks.md).

```go
KubernetesRunClusterLint(
    ctx context.Context,
    clusterId uuid.UUID,
    body *models.V2KubernetesClustersClusterlintRequest) (
    models.ApiResponse[models.V2KubernetesClustersClusterlintResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`*models.V2KubernetesClustersClusterlintRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-clusters-clusterlint-request.md) | Body, Optional | - |


# Response Type

**202**: The response is a JSON object with a key called `run_id` that you can later use to fetch the run results.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2KubernetesClustersClusterlintResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-clusters-clusterlint-response-1.md).


# Example Usage

```go
ctx := context.Background()

clusterId := uuid.MustParse("bd5f5959-5e1e-4205-a714-a914373942af")

body := models.V2KubernetesClustersClusterlintRequest{
    ExcludeChecks:         []string{
        "default-namespace",
    },
    ExcludeGroups:         []string{
        "workload-health",
    },
    IncludeChecks:         []string{
        "bare-pods",
        "resource-requirements",
    },
    IncludeGroups:         []string{
        "basic",
        "doks",
        "security",
    },
}

apiResponse, err := kubernetesApi.KubernetesRunClusterLint(ctx, clusterId, &body)
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



