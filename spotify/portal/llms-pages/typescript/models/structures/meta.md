# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type unknown.*


# Interface Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `analyzerVersion` | `string \| undefined` | Optional | The version of the Analyzer used to analyze this track. |
| `platform` | `string \| undefined` | Optional | The platform used to read the track's audio data. |
| `detailedStatus` | `string \| undefined` | Optional | A detailed status code for this track. If analysis data is missing, this code may explain why. |
| `statusCode` | `number \| undefined` | Optional | The return code of the analyzer process. 0 if successful, 1 if any errors occurred. |
| `timestamp` | `bigint \| undefined` | Optional | The Unix timestamp (in seconds) at which this track was analyzed. |
| `analysisTime` | `number \| undefined` | Optional | The amount of time taken to analyze this track. |
| `inputProcess` | `string \| undefined` | Optional | The method used to read the track's audio data. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  Meta,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const meta: Meta = {
  analyzerVersion: '4.0.0',
  platform: 'Linux',
  detailedStatus: 'OK',
  statusCode: 0,
  timestamp: BigInt(1495193577),
  analysisTime: 6.93906,
  inputProcess: 'libvorbisfile L+R 44100->22050',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



