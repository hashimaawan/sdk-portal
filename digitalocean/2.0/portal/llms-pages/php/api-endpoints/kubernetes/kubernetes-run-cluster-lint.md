# Kubernetes Run Cluster Lint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3J1bl9jbHVzdGVyTGludA

Clusterlint helps operators conform to Kubernetes best practices around
resources, security and reliability to avoid common problems while operating
or upgrading the clusters.

To request a clusterlint run on your cluster, send a POST request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/clusterlint`. This will run all
checks present in the `doks` group by default, if a request body is not
specified. Optionally specify the below attributes.

For information about the available checks, please refer to
[the clusterlint check documentation](https://github.com/digitalocean/clusterlint/blob/master/checks.md).

```php
function kubernetesRunClusterLint(
    string $clusterId,
    ?V2KubernetesClustersClusterlintRequest $body = null
): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `string` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`?V2KubernetesClustersClusterlintRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-kubernetes-clusters-clusterlint-request.md) | Body, Optional | - |


# Response Type

**202**: The response is a JSON object with a key called `run_id` that you can later use to fetch the run results.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2KubernetesClustersClusterlintResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-kubernetes-clusters-clusterlint-response-1.md).


# Example Usage

```php
$clusterId = 'bd5f5959-5e1e-4205-a714-a914373942af';

$body = V2KubernetesClustersClusterlintRequestBuilder::init()
    ->excludeChecks(
        [
            'default-namespace'
        ]
    )
    ->excludeGroups(
        [
            'workload-health'
        ]
    )
    ->includeChecks(
        [
            'bare-pods',
            'resource-requirements'
        ]
    )
    ->includeGroups(
        [
            'basic',
            'doks',
            'security'
        ]
    )
    ->build();

$kubernetesApi = $client->getKubernetesApi();
$apiResponse = $kubernetesApi->kubernetesRunClusterLint(
    $clusterId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2KubernetesClustersClusterlintResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



