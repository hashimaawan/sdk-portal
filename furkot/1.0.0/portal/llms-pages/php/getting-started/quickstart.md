# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/php/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)


# Building

The generated code has dependencies over external libraries like UniRest and JsonMapper. JsonMapper requires docblock annotations like `@var`, `@maps`, and `@factory` to map JSON responses with our class definitions. Hence the docblocks in generated code cannot be disabled by deactivating the PHP configurations like `opcache.save_comments`. These dependencies are defined in the `composer.json` file that comes with the SDK. To resolve these dependencies, we use the Composer package manager which requires PHP greater than or equal to 7.2 installed in your system. Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. Open command prompt and type `composer --version`. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including `composer.json`) for the SDK.
* Run the command `composer install`. This should install all the required dependencies and create the `vendor` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=installDependencies)

## Configuring CURL Certificate Path in php.ini

:information_source: **Note** This is for Windows users only.

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```
[curl]; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
curl.cainfo = PATH_TO/cacert.pem
```


# Installation

The following section explains how to use the FurkotTripsLib library in a new project.

## 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=openIDE)

Click on `Open` in PhpStorm to browse to your generated SDK directory and then click `OK`.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=openProject0)

## 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=createDirectory)

Name the directory as "test".

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=nameDirectory)

Add a PHP file to this project.

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=createFile)

Name it "testSDK".

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=nameFile)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```php
require_once "vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file `autoload.php` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 5](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=projectFiles)

After this you can add code to initialize the client library and acquire the instance of a Api class. Sample code to initialize the client library and use the Api methods is given in the subsequent sections.

## 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open `Settings` from `File` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=openSettings)

Select `PHP` from within `Languages & Frameworks`.

![Run Test Project - Step 2](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=setInterpreter0)

Browse for Interpreters near the `Interpreter` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=setInterpreter1)

Once the interpreter is selected, click `OK`.

![Run Test Project - Step 4](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=setInterpreter2)

To run your project, right click on your PHP file inside your Test project and click on `Run`.

![Run Test Project - Step 5](https://apidocs.io/illustration/php?workspaceFolder=FurkotTrips&step=runProject)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| timeout | `int` | Timeout for API calls in seconds.<br>*Default*: `30` |
| enableRetries | `bool` | Whether to enable retries and backoff feature.<br>*Default*: `false` |
| numberOfRetries | `int` | The number of retries to make.<br>*Default*: `0` |
| retryInterval | `float` | The retry time interval between the endpoint calls.<br>*Default*: `1` |
| backOffFactor | `float` | Exponential backoff factor to increase interval between retries.<br>*Default*: `2` |
| maximumRetryWaitTime | `int` | The maximum wait time in seconds for overall retrying requests.<br>*Default*: `0` |
| retryOnTimeout | `bool` | Whether to retry on request timeout.<br>*Default*: `true` |
| httpStatusCodesToRetry | `array` | Http status codes to retry against.<br>*Default*: `408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524` |
| httpMethodsToRetry | `array` | Http methods to retry against.<br>*Default*: `'GET', 'PUT', 'GET', 'PUT'` |
| loggingConfiguration | [`LoggingConfigurationBuilder`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/sdk-infrastructure/configuration/loggingconfigurationbuilder.md) | Represents the logging configurations for API calls |
| proxyConfiguration | [`ProxyConfigurationBuilder`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/sdk-infrastructure/configuration/proxyconfigurationbuilder.md) | Represents the proxy configurations for API calls |
| furkotAuthAccessCodeCredentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/getting-started/quickstart/authorization.md) | The Credentials Setter for OAuth 2 Authorization Code Grant |
| furkotAuthImplicitCredentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/getting-started/quickstart/authorization.md) | The Credentials Setter for OAuth 2 Implicit Grant |

The API client can be initialized as follows:

```php
use FurkotTripsLib\Logging\LoggingConfigurationBuilder;
use FurkotTripsLib\Logging\RequestLoggingConfigurationBuilder;
use FurkotTripsLib\Logging\ResponseLoggingConfigurationBuilder;
use Psr\Log\LogLevel;
use FurkotTripsLib\Environment;
use FurkotTripsLib\Authentication\FurkotAuthAccessCodeCredentialsBuilder;
use FurkotTripsLib\Models\OauthScopeFurkotAuthAccessCode;
use FurkotTripsLib\Authentication\FurkotAuthImplicitCredentialsBuilder;
use FurkotTripsLib\Models\OauthScopeFurkotAuthImplicit;
use FurkotTripsLib\FurkotTripsClientBuilder;

$client = FurkotTripsClientBuilder::init()
    ->furkotAuthAccessCodeCredentials(
        FurkotAuthAccessCodeCredentialsBuilder::init(
            'OAuthClientId',
            'OAuthClientSecret',
            'OAuthRedirectUri'
        )
            ->oauthScopes(
                [
                    OauthScopeFurkotAuthAccessCode::READTRIPS
                ]
            )
    )
    ->furkotAuthImplicitCredentials(
        FurkotAuthImplicitCredentialsBuilder::init(
            'OAuthClientId',
            'OAuthRedirectUri'
        )
            ->oauthScopes(
                [
                    OauthScopeFurkotAuthImplicit::READTRIPS
                ]
            )
    )
    ->environment(Environment::PRODUCTION)
    ->loggingConfiguration(
        LoggingConfigurationBuilder::init()
            ->level(LogLevel::INFO)
            ->requestConfiguration(RequestLoggingConfigurationBuilder::init()->body(true))
            ->responseConfiguration(ResponseLoggingConfigurationBuilder::init()->headers(true))
    )
    ->build();
```


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| OAuthClientId | `string` | OAuth 2 Client ID | `oauthClientId` | `getOauthClientId()` |
| OAuthClientSecret | `string` | OAuth 2 Client Secret | `oauthClientSecret` | `getOauthClientSecret()` |
| OAuthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `oauthRedirectUri` | `getOauthRedirectUri()` |
| OAuthToken | `OauthToken\|null` | Object for storing information about the OAuth token | `oauthToken` | `getOauthToken()` |
| OAuthScopes | `string[]\|null` | List of scopes that apply to the OAuth token | `oauthScopes` | `getOauthScopes()` |
| OAuthClockSkew | `int` | Clock skew time in seconds applied while checking the OAuth Token expiry. | `oauthClockSkew` | - |



**Note:** Auth credentials can be set using `FurkotAuthAccessCodeCredentialsBuilder::init()` in `furkotAuthAccessCodeCredentials` method in the client builder and accessed through `getFurkotAuthAccessCodeCredentials` method in the client instance.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```php
use FurkotTripsLib\Authentication\FurkotAuthAccessCodeCredentialsBuilder;
use FurkotTripsLib\Models\OauthScopeFurkotAuthAccessCode;
use FurkotTripsLib\FurkotTripsClientBuilder;

$client = FurkotTripsClientBuilder::init()
    ->furkotAuthAccessCodeCredentials(
        FurkotAuthAccessCodeCredentialsBuilder::init(
            'OAuthClientId',
            'OAuthClientSecret',
            'OAuthRedirectUri'
        )
            ->oauthScopes(
                [
                    OauthScopeFurkotAuthAccessCode::READTRIPS
                ]
            )
    )
    ->build();
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```php
$authUrl = $client->getFurkotAuthAccessCodeCredentials()->buildAuthorizationUrl();
header('Location: ' . filter_var($authUrl, FILTER_SANITIZE_URL));
```

### 3\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

If the user approves the request, the authorization code will be sent as the `code` query string:

```
https://example.com/oauth/callback?code=XXXXXXXXXXXXXXXXXXXXXXXXX
```

If the user does not approve the request, the response contains an `error` query string:

```
https://example.com/oauth/callback?error=access_denied
```

### 4\. Authorize the client using the code

After the server receives the code, it can exchange this for an *access token*. The access token is an object containing information for authorizing client requests and refreshing the token itself.

```php
try {
    $token = $client->getFurkotAuthAccessCodeCredentials()->fetchToken($_GET['code']);
    // re-build the client with oauth token
    $client = $client
        ->toBuilder()
        ->furkotAuthAccessCodeCredentials($client->getFurkotAuthAccessCodeCredentialsBuilder()->oauthToken($token))
        ->build();
} catch (FurkotTripsLib\Exceptions\ApiException $e) {
    // handle exception
}
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScopeFurkotAuthAccessCode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/models/enumerations/oauth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```php
if ($client->getFurkotAuthAccessCodeCredentials()->isTokenExpired()) {
    try {
        $token = $client->getFurkotAuthAccessCodeCredentials()->refreshToken();
        // re-build the client with oauth token
        $client = $client
            ->toBuilder()
            ->furkotAuthAccessCodeCredentials(
                $client->getFurkotAuthAccessCodeCredentialsBuilder()->oauthToken($token)
            )
            ->build();
    } catch (FurkotTripsLib\Exceptions\ApiException $e) {
        // handle exception
    }
}
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```php
// store token
$_SESSION['access_token'] = $client->getFurkotAuthAccessCodeCredentials()->getOauthToken();
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```php
// load token later...
$token = $_SESSION['access_token'];

// re-build the client with oauth token
$client = $client
    ->toBuilder()
    ->furkotAuthAccessCodeCredentials($client->getFurkotAuthAccessCodeCredentialsBuilder()->oauthToken($token))
    ->build();
```

### Complete example



```php
<?php
require_once __DIR__.'/vendor/autoload.php';

session_start();

use FurkotTripsLib\Logging\LoggingConfigurationBuilder;
use FurkotTripsLib\Logging\RequestLoggingConfigurationBuilder;
use FurkotTripsLib\Logging\ResponseLoggingConfigurationBuilder;
use Psr\Log\LogLevel;
use FurkotTripsLib\Environment;
use FurkotTripsLib\Authentication\FurkotAuthAccessCodeCredentialsBuilder;
use FurkotTripsLib\Models\OauthScopeFurkotAuthAccessCode;
use FurkotTripsLib\FurkotTripsClientBuilder;

$client = FurkotTripsClientBuilder::init()
    ->furkotAuthAccessCodeCredentials(
        FurkotAuthAccessCodeCredentialsBuilder::init(
            'OAuthClientId',
            'OAuthClientSecret',
            'OAuthRedirectUri'
        )
            ->oauthScopes(
                [
                    OauthScopeFurkotAuthAccessCode::READTRIPS
                ]
            )
    )
    ->environment(Environment::PRODUCTION)
    ->loggingConfiguration(
        LoggingConfigurationBuilder::init()
            ->level(LogLevel::INFO)
            ->requestConfiguration(RequestLoggingConfigurationBuilder::init()->body(true))
            ->responseConfiguration(ResponseLoggingConfigurationBuilder::init()->headers(true))
    )
    ->build();


// Obtain access token, restore from cache if possible
if (isset($_SESSION['access_token'])) {
    $token = $_SESSION['access_token'];
    // re-build the client with oauth token
    $client = $client
        ->toBuilder()
        ->furkotAuthAccessCodeCredentials($client->getFurkotAuthAccessCodeCredentialsBuilder()->oauthToken($token))
        ->build();
} else {
    try {
        // build authorization url to redirect the user
        $oAuthRedirectUri = $client->getFurkotAuthAccessCodeCredentials()->buildAuthorizationUrl();
        // redirect the user to $oAuthRedirectUri and get a code after the user consent
        header('Location: ' . filter_var($oAuthRedirectUri, FILTER_SANITIZE_URL));

        // fetch an oauth token to authorize the client using the stored code
        $token = $client->getFurkotAuthAccessCodeCredentials()->fetchToken($_GET['code']);
        // re-build the client with oauth token
        $client = $client
            ->toBuilder()
            ->furkotAuthAccessCodeCredentials(
                $client->getFurkotAuthAccessCodeCredentialsBuilder()->oauthToken($token)
            )
            ->build();

        // store token
        $_SESSION['access_token'] = $token;
    } catch (FurkotTripsLib\Exceptions\ApiException $e) {
        // handle exception
    }
}

// check if token gets expired, then try to refresh the token
if ($client->getFurkotAuthAccessCodeCredentials()->isTokenExpired()) {
    try {
        // refresh the token
        $token = $client->getFurkotAuthAccessCodeCredentials()->refreshToken();
        // re-build the client with oauth token
        $client = $client
            ->toBuilder()
            ->furkotAuthAccessCodeCredentials(
                $client->getFurkotAuthAccessCodeCredentialsBuilder()->oauthToken($token)
            )
            ->build();

        // update the cached token
        $_SESSION['access_token'] = $token;
    } catch (FurkotTripsLib\Exceptions\ApiException $e) {
        // handle exception
    }
}

// the client is now authorized; you can use $client to make endpoint calls
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```php
$authUrl = $client->getFurkotAuthImplicitCredentials()->buildAuthorizationUrl();
header('Location: ' . filter_var($authUrl, FILTER_SANITIZE_URL));
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScopeFurkotAuthImplicit`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/models/enumerations/oauth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list users trips info |




