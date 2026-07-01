# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)


# Building

## Requirements

The SDK relies on **Node.js** and **npm** (to resolve dependencies). It also requires **Typescript version >=4.1**. You can download and install Node.js and [npm](https://www.npmjs.com/) from [the official Node.js website](https://nodejs.org/en/download/).

> **NOTE:** npm is installed by default when Node.js is installed.

## Verify Successful Installation

Run the following commands in the command prompt or shell of your choice to check if Node.js and npm are successfully installed:

* Node.js: `node --version`

* npm: `npm --version`

![Version Check](https://apidocs.io/illustration/typescript?workspaceFolder=FurkotTrips&step=versionCheck)

## Install Dependencies

- To resolve all dependencies, go to the **SDK root directory** and run the following command with npm:

```bash
npm install
```

- This will install all dependencies in the **node_modules** folder.

![Resolve Dependencies](https://apidocs.io/illustration/typescript?workspaceFolder=FurkotTrips&workspaceName=furkot-tripslib&step=resolveDependency)


# Installation

The following section explains how to use the generated library in a new project.

## 1. Initialize the Node Project

- Open an IDE/text editor for JavaScript like Visual Studio Code. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

- Click on **File** and select **Open Folder**. Select an empty folder of your project, the folder will become visible in the sidebar on the left.

![Open Folder](https://apidocs.io/illustration/typescript?step=openProject)

- To initialize the Node project, click on **Terminal** and select **New Terminal**. Execute the following command in the terminal:

```bash
npm init --y
```

![Initialize the Node Project](https://apidocs.io/illustration/typescript?step=initializeProject)

## 2. Add Dependencies to the Client Library

- The created project manages its dependencies using its `package.json` file. In order to add a dependency on the *Furkot TripsLib* client library, double click on the `package.json` file in the bar on the left and add the dependency to the package in it.

![Add FurkotTripslib Dependency](https://apidocs.io/illustration/typescript?workspaceFolder=FurkotTrips&workspaceName=furkot-tripslib&step=importDependency)

- To install the package in the project, run the following command in the terminal:

```bash
npm install
```

![Install FurkotTripslib Dependency](https://apidocs.io/illustration/typescript?step=installDependency)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `30000` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/httpclientoptions.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/partialloggingoptions.md) | Logging Configuration to enable logging |
| furkotAuthAccessCodeCredentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md) | The credential object for furkotAuthAccessCode |
| furkotAuthImplicitCredentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md) | The credential object for furkotAuthImplicit |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ts
import {
  Client,
  Environment,
  LogLevel,
  OauthScopeFurkotAuthAccessCode,
  OauthScopeFurkotAuthImplicit,
} from 'furkot-tripslib';

const client = new Client({
  furkotAuthAccessCodeCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthClientSecret: 'OAuthClientSecret',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScopeFurkotAuthAccessCode.Readtrips
    ]
  },
  furkotAuthImplicitCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScopeFurkotAuthImplicit.Readtrips
    ]
  },
  timeout: 30000,
  environment: Environment.Production,
  logging: {
    logLevel: LogLevel.Info,
    logRequest: {
      logBody: true
    },
    logResponse: {
      logHeaders: true
    }
  },
});
```

## Configuration-Based Client Initialization

```ts
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'furkot-tripslib';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/configuration-based-client-initialization.md) section for details.

## Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'furkot-tripslib';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| oauthClientId | `string` | OAuth 2 Client ID | `oauthClientId` |
| oauthClientSecret | `string` | OAuth 2 Client Secret | `oauthClientSecret` |
| oauthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `oauthRedirectUri` |
| oauthToken | `OauthToken` | Object for storing information about the OAuth token | `oauthToken` |
| oauthScopes | `OauthScopeFurkotAuthAccessCode[]` | List of scopes that apply to the OAuth token | `oauthScopes` |
| oauthClockSkew | `number` | Clock skew time in seconds applied while checking the OAuth Token expiry. | `clockSkew` |
| oauthTokenProvider | `(lastOAuthToken: OauthToken \| undefined, authManager: FurkotAuthAccessCodeManager) => Promise<OauthToken>` | Registers a callback for oAuth Token Provider used for automatic token fetching/refreshing. | `oauthTokenProvider` |
| oauthOnTokenUpdate | `(token: OauthToken) => void` | Registers a callback for token update event. | `oauthOnTokenUpdate` |



**Note:** Auth credentials can be set using `furkotAuthAccessCodeCredentials` object in the client.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```ts
import { Client, OauthScopeFurkotAuthAccessCode } from 'furkot-tripslib';

const client = new Client({
  furkotAuthAccessCodeCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthClientSecret: 'OAuthClientSecret',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScopeFurkotAuthAccessCode.Readtrips
    ]
  },
});
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```ts
const authUrl = client.furkotAuthAccessCodeManager?.buildAuthorizationUrl();
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

```ts
try {
  const token = await client.furkotAuthAccessCodeManager?.fetchToken(authorizationCode);
  if (token) {
    client.withConfiguration({
      furkotAuthAccessCodeCredentials: {
        ...config.furkotAuthAccessCodeCredentials,
        oauthToken: token
      }
    });
  }
} catch(error) {
  // handle ApiError or OAuthProviderError if needed
}
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScopeFurkotAuthAccessCode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/models/enumerations/oauth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `Readtrips` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```ts
try {
  const token = await client.furkotAuthAccessCodeManager?.refreshToken();
} catch(error) {
  // handle error
}
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```ts
Store the token in session storage or local storage.
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```ts
const newClient = client.withConfiguration({
  furkotAuthAccessCodeCredentials: {
    ...config.furkotAuthAccessCodeCredentials,
    oauthToken: token
  }
});
```

### Complete example



```ts
import {
  Client,
  OauthScopeFurkotAuthAccessCode,
  OauthToken,
} from 'furkot-tripslib';

// function for storing token to database
async function saveTokenToDatabase(token: OAuthToken) {
  // Code to save the token to the database
}

// function for loading token from database
async function loadTokenFromDatabase(): Promise<OAuthToken | undefined> {
  // Load token from the database and return it (return undefined if no token exists)
  return undefined;
}

// create a new client from configuration
const client = new Client({
  furkotAuthAccessCodeCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthClientSecret: 'OAuthClientSecret',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScopeFurkotAuthAccessCode.Readtrips
    ]
  },
});

// obtain access token, needed for client to be authorized
const previousToken = await loadTokenFromDatabase();
if (previousToken) {
  // restore previous access token and update the cloned configuration with the token
  client.withConfiguration({
    furkotAuthAccessCodeCredentials: {
      ...config.furkotAuthAccessCodeCredentials,
      oauthToken: previousToken
    }
  });
}
else {
    // redirect user to a page that handles authorization
}
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```ts
const authUrl = client.furkotAuthImplicitManager?.buildAuthorizationUrl();
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScopeFurkotAuthImplicit`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/models/enumerations/oauth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `Readtrips` | list users trips info |




