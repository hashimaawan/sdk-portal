# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

<p>Amazon Athena is an interactive query service that lets you use standard SQL to analyze data directly in Amazon S3. You can point Athena at your data in Amazon S3 and run ad-hoc queries and get results in seconds. Athena is serverless, so there is no infrastructure to set up or manage. You pay only for the queries you run. Athena scales automatically—executing queries in parallel—so results are fast, even with large datasets and complex queries. For more information, see <a href="http://docs.aws.amazon.com/athena/latest/ug/what-is.html">What is Amazon Athena</a> in the <i>Amazon Athena User Guide</i>.</p> <p>If you connect to Athena using the JDBC driver, use version 1.1.0 of the driver or later with the Amazon Athena API. Earlier version drivers do not support the API. For more information and to download the driver, see <a href="https://docs.aws.amazon.com/athena/latest/ug/connect-with-jdbc.html">Accessing Amazon Athena with JDBC</a>.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="https://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


Amazon Web Services documentation: [https://docs.aws.amazon.com/athena/](https://docs.aws.amazon.com/athena/)


# Building

## Requirements

The SDK relies on **Node.js** and **npm** (to resolve dependencies). It also requires **Typescript version >=4.1**. You can download and install Node.js and [npm](https://www.npmjs.com/) from [the official Node.js website](https://nodejs.org/en/download/).

> **NOTE:** npm is installed by default when Node.js is installed.

## Verify Successful Installation

Run the following commands in the command prompt or shell of your choice to check if Node.js and npm are successfully installed:

* Node.js: `node --version`

* npm: `npm --version`

![Version Check](https://apidocs.io/illustration/typescript?workspaceFolder=AmazonAthena&step=versionCheck)

## Install Dependencies

- To resolve all dependencies, go to the **SDK root directory** and run the following command with npm:

```bash
npm install
```

- This will install all dependencies in the **node_modules** folder.

![Resolve Dependencies](https://apidocs.io/illustration/typescript?workspaceFolder=AmazonAthena&workspaceName=amazon-athenalib&step=resolveDependency)


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

- The created project manages its dependencies using its `package.json` file. In order to add a dependency on the *Amazon AthenaLib* client library, double click on the `package.json` file in the bar on the left and add the dependency to the package in it.

![Add AmazonAthenalib Dependency](https://apidocs.io/illustration/typescript?workspaceFolder=AmazonAthena&workspaceName=amazon-athenalib&step=importDependency)

- To install the package in the project, run the following command in the terminal:

```bash
npm install
```

![Install AmazonAthenalib Dependency](https://apidocs.io/illustration/typescript?step=installDependency)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** The Amazon Athena multi-region endpoint |
| Environment2 | The Amazon Athena multi-region endpoint |
| Environment3 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |
| Environment4 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| region | `Region` | The AWS region<br>*Default*: `Region.Useast1` |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `30000` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/httpclientoptions.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/partialloggingoptions.md) | Logging Configuration to enable logging |
| customHeaderAuthenticationCredentials | [`CustomHeaderAuthenticationCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md) | The credential object for customHeaderAuthentication |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ts
import { Client, Environment, LogLevel, Region } from 'amazon-athenalib';

const client = new Client({
  customHeaderAuthenticationCredentials: {
    'Authorization': 'Authorization'
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
  region: Region.Useast1,
});
```

## Configuration-Based Client Initialization

```ts
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'amazon-athenalib';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/configuration-based-client-initialization.md) section for details.

## Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'amazon-athenalib';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`hmac (Custom Header Signature)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)

## hmac (Custom Header Signature)



Documentation for accessing and setting credentials for hmac.

### Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| Authorization | `string` | Amazon Signature authorization v4 | `authorization` |



**Note:** Auth credentials can be set using `customHeaderAuthenticationCredentials` object in the client.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ts
import { Client } from 'amazon-athenalib';

const client = new Client({
  customHeaderAuthenticationCredentials: {
    'Authorization': 'Authorization'
  },
});
```




