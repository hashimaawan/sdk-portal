# Create an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkNyZWF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Creates a new SSH key with the given `name` and `public_key`. Once an SSH key is created, it can be used in other calls such as creating Servers.

:information_source: **Note** This endpoint does not require authentication.

```php
function createAnSshKey(?SshKeysRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?SshKeysRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ssh-keys-request.md) | Body, Optional | - |


# Response Type

**201**: The `ssh_key` key in the reply contains the object that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ssh-keys-response-1.md).


# Example Usage

```php
$body = SshKeysRequestBuilder::init(
    'My ssh key',
    'ssh-rsa AAAjjk76kgf...Xt'
)->build();

$sshKeysApi = $client->getSshKeysApi();
$apiResponse = $sshKeysApi->createAnSshKey($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'SshKeysResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



