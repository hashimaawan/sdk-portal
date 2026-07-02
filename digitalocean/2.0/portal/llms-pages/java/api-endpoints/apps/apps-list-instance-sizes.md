# Apps List Instance Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3RfaW5zdGFuY2VTaXplcw

List all instance sizes for `service`, `worker`, and `job` components.

```java
CompletableFuture<ApiResponse<V2AppsTiersInstanceSizesResponse>> appsListInstanceSizesAsync()
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Response Type

**200**: A JSON with key `instance_sizes`

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2AppsTiersInstanceSizesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-apps-tiers-instance-sizes-response.md).


# Example Usage

```java
appsApi.appsListInstanceSizesAsync().thenAccept(result -> {
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


# Example Response *(as JSON)*

```json
{
  "instance_sizes": [
    {
      "cpu_type": "SHARED",
      "cpus": "1",
      "memory_bytes": "536870912",
      "name": "Basic XXS",
      "slug": "basic-xxs",
      "tier_slug": "basic",
      "tier_upgrade_to": "professional-xs",
      "usd_per_month": "5.00",
      "usd_per_second": "0.000002066799"
    },
    {
      "cpu_type": "SHARED",
      "cpus": "1",
      "memory_bytes": "1073741824",
      "name": "Basic XS",
      "slug": "basic-xs",
      "tier_slug": "basic",
      "tier_upgrade_to": "professional-xs",
      "usd_per_month": "10.00",
      "usd_per_second": "0.000004133598"
    },
    {
      "cpu_type": "SHARED",
      "cpus": "1",
      "memory_bytes": "2147483648",
      "name": "Basic S",
      "slug": "basic-s",
      "tier_slug": "basic",
      "tier_upgrade_to": "professional-s",
      "usd_per_month": "20.00",
      "usd_per_second": "0.000008267196"
    },
    {
      "cpu_type": "SHARED",
      "cpus": "2",
      "memory_bytes": "4294967296",
      "name": "Basic M",
      "slug": "basic-m",
      "tier_slug": "basic",
      "tier_upgrade_to": "professional-m",
      "usd_per_month": "40.00",
      "usd_per_second": "0.000016534392"
    },
    {
      "cpu_type": "SHARED",
      "cpus": "1",
      "memory_bytes": "1073741824",
      "name": "Professional XS",
      "slug": "professional-xs",
      "tier_downgrade_to": "basic-xs",
      "tier_slug": "professional",
      "usd_per_month": "12.00",
      "usd_per_second": "0.000004960317"
    },
    {
      "cpu_type": "SHARED",
      "cpus": "1",
      "memory_bytes": "2147483648",
      "name": "Professional S",
      "slug": "professional-s",
      "tier_downgrade_to": "basic-s",
      "tier_slug": "professional",
      "usd_per_month": "25.00",
      "usd_per_second": "0.000010333995"
    },
    {
      "cpu_type": "SHARED",
      "cpus": "2",
      "memory_bytes": "4294967296",
      "name": "Professional M",
      "slug": "professional-m",
      "tier_downgrade_to": "basic-s",
      "tier_slug": "professional",
      "usd_per_month": "50.00",
      "usd_per_second": "0.000020667989"
    },
    {
      "cpu_type": "DEDICATED",
      "cpus": "1",
      "memory_bytes": "4294967296",
      "name": "Professional 1L",
      "slug": "professional-1l",
      "tier_downgrade_to": "basic-m",
      "tier_slug": "professional",
      "usd_per_month": "75.00",
      "usd_per_second": "0.000031001984"
    },
    {
      "cpu_type": "DEDICATED",
      "cpus": "2",
      "memory_bytes": "8589934592",
      "name": "Professional L",
      "slug": "professional-l",
      "tier_downgrade_to": "basic-s",
      "tier_slug": "professional",
      "usd_per_month": "150.00",
      "usd_per_second": "0.000062003968"
    },
    {
      "cpu_type": "DEDICATED",
      "cpus": "4",
      "memory_bytes": "17179869184",
      "name": "Professional XL",
      "slug": "professional-xl",
      "tier_downgrade_to": "basic-s",
      "tier_slug": "professional",
      "usd_per_month": "300.00",
      "usd_per_second": "0.000124007937"
    }
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



