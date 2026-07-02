# Kubernetes Destroy Associated Resources Selective

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2Rlc3Ryb3lfYXNzb2NpYXRlZFJlc291cmNlc1NlbGVjdGl2ZQ

To delete a Kubernetes cluster along with a subset of its associated resources,
send a DELETE request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/destroy_with_associated_resources/selective`.

The JSON body of the request should include `load_balancers`, `volumes`, or
`volume_snapshots` keys each set to an array of IDs for the associated
resources to be destroyed.

The IDs can be found by querying the cluster's associated resources endpoint.
Any associated resource not included in the request will remain and continue
to accrue changes on your account.

```java
CompletableFuture<ApiResponse<Void>> kubernetesDestroyAssociatedResourcesSelectiveAsync(
    final UUID clusterId,
    final V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-kubernetes-clusters-destroy-with-associated-resources-selective-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
UUID clusterId = UUID.fromString("bd5f5959-5e1e-4205-a714-a914373942af");
V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest body = new V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest.Builder()
    .loadBalancers(Arrays.asList(
        "4de7ac8b-495b-4884-9a69-1050c6793cd6"
    ))
    .volumeSnapshots(Arrays.asList(
        "edb0478d-7436-11ea-86e6-0a58ac144b91"
    ))
    .volumes(Arrays.asList(
        "ba49449a-7435-11ea-b89e-0a58ac14480f"
    ))
    .build();

kubernetesApi.kubernetesDestroyAssociatedResourcesSelectiveAsync(clusterId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



