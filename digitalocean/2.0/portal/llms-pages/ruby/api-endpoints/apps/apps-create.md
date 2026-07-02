# Apps Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZQ

Create a new app by submitting an app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).

```ruby
def apps_create(body,
                accept: nil,
                content_type: nil)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-apps-request.md) | Body, Required | - |
| `accept` | [`Accept`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/accept.md) | Header, Optional | The content-type that should be used by the response. By default, the response will be `application/json`. `application/yaml` is also supported. |
| `content_type` | [`ContentType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/content-type.md) | Header, Optional | The content-type used for the request. By default, the requests are assumed to use `application/json`. `application/yaml` is also supported. |


# Response Type

**200**: A JSON or YAML of a `spec` object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2AppsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-apps-response-1.md).


# Example Usage

```ruby
body = V2AppsRequest.new(
  spec: AppSpec.new(
    name: 'web-app',
    region: Region1::NYC,
    services: [
      Service.new(
        name: 'api',
        environment_slug: 'node-js',
        github: Github.new(
          branch: 'main',
          deploy_on_push: true,
          repo: 'digitalocean/sample-golang'
        ),
        run_command: 'bin/api',
        instance_count: 2,
        instance_size_slug: InstanceSizeSlug::BASICXXS,
        routes: [
          ACriterionForRoutingHttpTrafficToAComponent.new(
            path: '/api'
          )
        ]
      )
    ]
  )
)

accept = Accept::ENUM_APPLICATIONJSON

content_type = ContentType::ENUM_APPLICATIONJSON

result = apps_api.apps_create(
  body,
  accept: accept,
  content_type: content_type
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



