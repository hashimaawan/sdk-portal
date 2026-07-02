# Registry Delete Repository Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZyZWdpc3RyeV9kZWxldGVfcmVwb3NpdG9yeVRhZw

To delete a container repository tag, send a DELETE request to
`/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags/$TAG`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to delete
`registry.digitalocean.com/example/my/repo:mytag`, the path would be
`/v2/registry/example/repositories/my%2Frepo/tags/mytag`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.

```go
RegistryDeleteRepositoryTag(
    ctx context.Context,
    registryName string,
    repositoryName string,
    repositoryTag string) (
    http.Response,
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registryName` | `string` | Template, Required | The name of a container registry. |
| `repositoryName` | `string` | Template, Required | The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`. |
| `repositoryTag` | `string` | Template, Required | The name of a container registry repository tag. |


# Response Type

**204**: The action was successful and the response body is empty.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

registryName := "example"

repositoryName := "repo-1"

repositoryTag := "06a447a"

resp, err := containerRegistryApi.RegistryDeleteRepositoryTag(ctx, registryName, repositoryName, repositoryTag)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    fmt.Println(resp.StatusCode)
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



