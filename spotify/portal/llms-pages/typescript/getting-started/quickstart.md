# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

You can use Spotify's Web API to discover music and podcasts, manage your Spotify library, control audio playback, and much more. Browse our available Web API endpoints using the sidebar at left, or via the navigation bar on top of this page on smaller screens.

In order to make successful Web API requests your app will need a valid access token. One can be obtained through <a href="https://developer.spotify.com/documentation/general/guides/authorization-guide/">OAuth 2.0</a>.

The base URI for all Web API requests is `https://api.spotify.com/v1`.

Need help? See our <a href="https://developer.spotify.com/documentation/web-api/guides/">Web API guides</a> for more information, or visit the <a href="https://community.spotify.com/t5/Spotify-for-Developers/bd-p/Spotify_Developer">Spotify for Developers community forum</a> to ask questions and connect with other developers.


# Building

## Requirements

The SDK relies on **Node.js** and **npm** (to resolve dependencies). It also requires **Typescript version >=4.1**. You can download and install Node.js and [npm](https://www.npmjs.com/) from [the official Node.js website](https://nodejs.org/en/download/).

> **NOTE:** npm is installed by default when Node.js is installed.

## Verify Successful Installation

Run the following commands in the command prompt or shell of your choice to check if Node.js and npm are successfully installed:

* Node.js: `node --version`

* npm: `npm --version`

![Version Check](https://apidocs.io/illustration/typescript?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&step=versionCheck)

## Install Dependencies

- To resolve all dependencies, go to the **SDK root directory** and run the following command with npm:

```bash
npm install
```

- This will install all dependencies in the **node_modules** folder.

![Resolve Dependencies](https://apidocs.io/illustration/typescript?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&workspaceName=spotify-web-api-with-fixes-and-improvements-from-sonalluxlib&step=resolveDependency)


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

- The created project manages its dependencies using its `package.json` file. In order to add a dependency on the *Spotify Web API with fixes and improvements from sonalluxLib* client library, double click on the `package.json` file in the bar on the left and add the dependency to the package in it.

![Add SpotifyWebApiWithFixesAndImprovementsFromSonalluxlib Dependency](https://apidocs.io/illustration/typescript?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&workspaceName=spotify-web-api-with-fixes-and-improvements-from-sonalluxlib&step=importDependency)

- To install the package in the project, run the following command in the terminal:

```bash
npm install
```

![Install SpotifyWebApiWithFixesAndImprovementsFromSonalluxlib Dependency](https://apidocs.io/illustration/typescript?step=installDependency)


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
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `30000` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/sdk-infrastructure/configuration/httpclientoptions.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/sdk-infrastructure/configuration/partialloggingoptions.md) | Logging Configuration to enable logging |
| authorizationCodeAuthCredentials | [`AuthorizationCodeAuthCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/getting-started/quickstart/authorization.md) | The credential object for authorizationCodeAuth |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ts
import {
  Client,
  Environment,
  LogLevel,
  OauthScope,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const client = new Client({
  authorizationCodeAuthCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthClientSecret: 'OAuthClientSecret',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScope.AppRemoteControl,
      OauthScope.PlaylistReadPrivate
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
import { Client } from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/sdk-infrastructure/configuration/configuration-based-client-initialization.md) section for details.

## Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`oauth_2_0 (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)

## oauth_2_0 (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for oauth_2_0.

### Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| oauthClientId | `string` | OAuth 2 Client ID | `oauthClientId` |
| oauthClientSecret | `string` | OAuth 2 Client Secret | `oauthClientSecret` |
| oauthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `oauthRedirectUri` |
| oauthToken | `OauthToken` | Object for storing information about the OAuth token | `oauthToken` |
| oauthScopes | `OauthScope[]` | List of scopes that apply to the OAuth token | `oauthScopes` |
| oauthClockSkew | `number` | Clock skew time in seconds applied while checking the OAuth Token expiry. | `clockSkew` |
| oauthTokenProvider | `(lastOAuthToken: OauthToken \| undefined, authManager: AuthorizationCodeAuthManager) => Promise<OauthToken>` | Registers a callback for oAuth Token Provider used for automatic token fetching/refreshing. | `oauthTokenProvider` |
| oauthOnTokenUpdate | `(token: OauthToken) => void` | Registers a callback for token update event. | `oauthOnTokenUpdate` |



**Note:** Auth credentials can be set using `authorizationCodeAuthCredentials` object in the client.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```ts
import {
  Client,
  OauthScope,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const client = new Client({
  authorizationCodeAuthCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthClientSecret: 'OAuthClientSecret',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScope.AppRemoteControl,
      OauthScope.PlaylistReadPrivate
    ]
  },
});
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```ts
const authUrl = client.authorizationCodeAuthManager?.buildAuthorizationUrl();
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
  const token = await client.authorizationCodeAuthManager?.fetchToken(authorizationCode);
  if (token) {
    client.withConfiguration({
      authorizationCodeAuthCredentials: {
        ...config.authorizationCodeAuthCredentials,
        oauthToken: token
      }
    });
  }
} catch(error) {
  // handle ApiError or OAuthProviderError if needed
}
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScope`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/enumerations/oauth-scope.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `AppRemoteControl` | Communicate with the Spotify app on your device. |
| `PlaylistReadPrivate` | Access your private playlists. |
| `PlaylistReadCollaborative` | Access your collaborative playlists. |
| `PlaylistModifyPublic` | Manage your public playlists. |
| `PlaylistModifyPrivate` | Manage your private playlists. |
| `UserLibraryRead` | Access your saved content. |
| `UserLibraryModify` | Manage your saved content. |
| `UserReadPrivate` | Access your subscription details. |
| `UserReadEmail` | Get your real email address. |
| `UserFollowRead` | Access your followers and who you are following. |
| `UserFollowModify` | Manage your saved content. |
| `UserTopRead` | Read your top artists and content. |
| `UserReadPlaybackPosition` | Read your position in content you have played. |
| `UserReadPlaybackState` | Read your currently playing content and Spotify Connect devices information. |
| `UserReadRecentlyPlayed` | Access your recently played items. |
| `UserReadCurrentlyPlaying` | Read your currently playing content. |
| `UserModifyPlaybackState` | Control playback on your Spotify clients and Spotify Connect devices. |
| `UgcImageUpload` | Upload images to Spotify on your behalf. |
| `Streaming` | Play content and control playback on your other devices. |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```ts
try {
  const token = await client.authorizationCodeAuthManager?.refreshToken();
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
  authorizationCodeAuthCredentials: {
    ...config.authorizationCodeAuthCredentials,
    oauthToken: token
  }
});
```

### Complete example



```ts
import {
  Client,
  OauthScope,
  OauthToken,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

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
  authorizationCodeAuthCredentials: {
    oauthClientId: 'OAuthClientId',
    oauthClientSecret: 'OAuthClientSecret',
    oauthRedirectUri: 'OAuthRedirectUri',
    oauthScopes: [
      OauthScope.AppRemoteControl,
      OauthScope.PlaylistReadPrivate
    ]
  },
});

// obtain access token, needed for client to be authorized
const previousToken = await loadTokenFromDatabase();
if (previousToken) {
  // restore previous access token and update the cloned configuration with the token
  client.withConfiguration({
    authorizationCodeAuthCredentials: {
      ...config.authorizationCodeAuthCredentials,
      oauthToken: previousToken
    }
  });
}
else {
    // redirect user to a page that handles authorization
}
```




