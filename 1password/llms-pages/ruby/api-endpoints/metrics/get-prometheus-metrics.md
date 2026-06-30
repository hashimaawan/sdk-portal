# Get Prometheus Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRk1ldHJpY3MlMkZHZXRQcm9tZXRoZXVzTWV0cmljcw

See Prometheus documentation for a complete data model.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_prometheus_metrics
```


# Response Type

**200**: Successfully returned Prometheus metrics

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type `String`.


# Example Usage

```ruby
result = metrics_api.get_prometheus_metrics

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



