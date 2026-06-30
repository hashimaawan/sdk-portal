# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/php/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type array.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `analyzerVersion` | `?string` | Optional | The version of the Analyzer used to analyze this track. | getAnalyzerVersion(): ?string | setAnalyzerVersion(?string analyzerVersion): void |
| `platform` | `?string` | Optional | The platform used to read the track's audio data. | getPlatform(): ?string | setPlatform(?string platform): void |
| `detailedStatus` | `?string` | Optional | A detailed status code for this track. If analysis data is missing, this code may explain why. | getDetailedStatus(): ?string | setDetailedStatus(?string detailedStatus): void |
| `statusCode` | `?int` | Optional | The return code of the analyzer process. 0 if successful, 1 if any errors occurred. | getStatusCode(): ?int | setStatusCode(?int statusCode): void |
| `timestamp` | `?int` | Optional | The Unix timestamp (in seconds) at which this track was analyzed. | getTimestamp(): ?int | setTimestamp(?int timestamp): void |
| `analysisTime` | `?float` | Optional | The amount of time taken to analyze this track. | getAnalysisTime(): ?float | setAnalysisTime(?float analysisTime): void |
| `inputProcess` | `?string` | Optional | The method used to read the track's audio data. | getInputProcess(): ?string | setInputProcess(?string inputProcess): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\MetaBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$meta = MetaBuilder::init()
    ->analyzerVersion('4.0.0')
    ->platform('Linux')
    ->detailedStatus('OK')
    ->statusCode(0)
    ->timestamp(1495193577)
    ->analysisTime(6.93906)
    ->inputProcess('libvorbisfile L+R 44100->22050')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



