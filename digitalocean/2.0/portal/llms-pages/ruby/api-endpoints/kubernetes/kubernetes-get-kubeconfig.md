# Kubernetes Get Kubeconfig

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2dldF9rdWJlY29uZmln

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

```ruby
def kubernetes_get_kubeconfig(cluster_id,
                              expiry_seconds: 0)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cluster_id` | `UUID \| String` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `expiry_seconds` | `Integer` | Query, Optional | The duration in seconds that the returned Kubernetes credentials will be valid. If not set or 0, the credentials will have a 7 day expiry.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |


# Response Type

**200**: A kubeconfig file for the cluster in YAML format.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type `Mixed`.


# Example Usage

```ruby
cluster_id = 'bd5f5959-5e1e-4205-a714-a914373942af'

expiry_seconds = 300

result = kubernetes_api.kubernetes_get_kubeconfig(
  cluster_id,
  expiry_seconds: expiry_seconds
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



