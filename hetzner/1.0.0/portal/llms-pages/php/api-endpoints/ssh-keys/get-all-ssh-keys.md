# Get All SSH Keys

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYWxsJTI1MjBTU0glMjUyMGtleXM

Returns all SSH key objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllSshKeys(
    ?string $sort = null,
    ?string $name = null,
    ?string $fingerprint = null,
    ?string $labelSelector = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`?string(Sort8)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort-8.md) | Query, Optional | Can be used multiple times. |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `fingerprint` | `?string` | Query, Optional | Can be used to filter SSH keys by their fingerprint. The response will only contain the SSH key matching the specified fingerprint. |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `ssh_keys` key in the reply contains an array of SSH key objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`SshKeysResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ssh-keys-response.md).


# Example Usage

```php
$sshKeysApi = $client->getSshKeysApi();
$apiResponse = $sshKeysApi->getAllSshKeys();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'SshKeysResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



