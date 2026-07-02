# Kubernetes Upgrade Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3VwZ3JhZGVfY2x1c3Rlcg

To immediately upgrade a Kubernetes cluster to a newer patch release of
Kubernetes, send a POST request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/upgrade`.
The body of the request must specify a version attribute.

Available upgrade versions for a cluster can be fetched from
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/upgrades`.

```php
function kubernetesUpgradeCluster(string $clusterId, V2KubernetesClustersUpgradeRequest $body): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `string` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`V2KubernetesClustersUpgradeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-kubernetes-clusters-upgrade-request.md) | Body, Required | - |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$clusterId = 'bd5f5959-5e1e-4205-a714-a914373942af';

$body = V2KubernetesClustersUpgradeRequestBuilder::init()
    ->version('1.16.13-do.0')
    ->build();

$kubernetesApi = $client->getKubernetesApi();
$apiResponse = $kubernetesApi->kubernetesUpgradeCluster(
    $clusterId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
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



