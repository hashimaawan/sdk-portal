# Get All Certificates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkdldCUyNTIwYWxsJTI1MjBDZXJ0aWZpY2F0ZXM

Returns all Certificate objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllCertificates(
    ?string $sort = null,
    ?string $name = null,
    ?string $labelSelector = null,
    ?string $type = null
): CertificatesResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`?string(SortEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `type` | [`?string(ParameterTypeEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/parameter-type.md) | Query, Optional | Can be used multiple times. The response will only contain Certificates matching the type. |


# Response Type

**200**: The `certificates` key contains an array of Certificate objects

[`CertificatesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/certificates-response.md)


# Example Usage

```php
$certificatesController = $client->getCertificatesController();

try {
    $result = $certificatesController->getAllCertificates();
    echo 'CertificatesResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Example Response *(as JSON)*

```json
{
  "certificates": [
    {
      "certificate": "-----BEGIN CERTIFICATE-----\n...",
      "created": "2019-01-08T12:10:00+00:00",
      "domain_names": [
        "example.com",
        "webmail.example.com",
        "www.example.com"
      ],
      "fingerprint": "03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f",
      "id": 897,
      "labels": {
        "env": "dev"
      },
      "name": "my website cert",
      "not_valid_after": "2019-07-08T09:59:59+00:00",
      "not_valid_before": "2019-01-08T10:00:00+00:00",
      "status": null,
      "type": "uploaded",
      "used_by": [
        {
          "id": 4711,
          "type": "load_balancer"
        }
      ]
    }
  ]
}
```



