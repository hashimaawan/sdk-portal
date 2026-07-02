# HttpProxyConfiguration.Builder

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRkh0dHBQcm94eUNvbmZpZ3VyYXRpb24uQnVpbGRlcg


Class to build instances of [HttpProxyConfiguration](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/configuration/httpproxyconfiguration.md).

# Constructors

| Name | Description |
|  --- | --- |
| `Builder()` | Default Constructor to initiate builder with default properties. |

# Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `Builder(String address, int port)` | Constructs HttpProxyConfiguration.Builder with proxy address and port. | `HttpProxyConfiguration.Builder` |
| `auth(String username, String password)` | Sets the username and password for proxy auth. | `HttpProxyConfiguration.Builder` |
| `build()` | Builds a new HttpProxyConfiguration object using the set fields. | [`HttpProxyConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/configuration/httpproxyconfiguration.md) |

## Client Initialization with Proxy Configuration

To configure the SDK to use a proxy server, initialize the proxy configuration during client setup as shown in the Usage Example.

# Usage Example

```java
import com.digitalocean.api.DigitalOceanApiClient;
import com.digitalocean.api.http.client.HttpProxyConfiguration;

DigitalOceanApiClient client = new DigitalOceanApiClient.Builder()
  .httpClientConfig(configBuilder -> configBuilder
      .proxyConfig(new HttpProxyConfiguration.Builder("http://localhost",
          8080).auth("username", "password")))
  .build();
```



