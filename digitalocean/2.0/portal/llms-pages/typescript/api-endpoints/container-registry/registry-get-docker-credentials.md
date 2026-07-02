# Registry Get Docker Credentials

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZyZWdpc3RyeV9nZXRfZG9ja2VyQ3JlZGVudGlhbHM

In order to access your container registry with the Docker client or from a
Kubernetes cluster, you will need to configure authentication. The necessary
JSON configuration can be retrieved by sending a GET request to
`/v2/registry/docker-credentials`.

The response will be in the format of a Docker `config.json` file. To use the
config in your Kubernetes cluster, create a Secret with:

    kubectl create secret generic docr \
      --from-file=.dockerconfigjson=config.json \
      --type=kubernetes.io/dockerconfigjson

By default, the returned credentials have read-only access to your registry
and cannot be used to push images. This is appropriate for most Kubernetes
clusters. To retrieve read/write credentials, suitable for use with the Docker
client or in a CI system, read_write may be provided as query parameter. For
example: `/v2/registry/docker-credentials?read_write=true`

By default, the returned credentials will not expire. To retrieve credentials
with an expiry set, expiry_seconds may be provided as a query parameter. For
example: `/v2/registry/docker-credentials?expiry_seconds=3600` will return
credentials that expire after one hour.

```ts
async registryGetDockerCredentials(
  expirySeconds?: number,
  readWrite?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2RegistryDockerCredentialsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `expirySeconds` | `number \| undefined` | Query, Optional | The duration in seconds that the returned registry credentials will be valid. If not set or 0, the credentials will not expire.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |
| `readWrite` | `boolean \| undefined` | Query, Optional | By default, the registry credentials allow for read-only access. Set this query parameter to `true` to obtain read-write credentials.<br><br>**Default**: `false` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A Docker `config.json` file for the container registry.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2RegistryDockerCredentialsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-registry-docker-credentials-response.md).


# Example Usage

```ts
const expirySeconds = 3600;

const readWrite = true;

try {
  const response = await containerRegistryApi.registryGetDockerCredentials(
    expirySeconds,
    readWrite
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
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



