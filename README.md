# Fiks Innsyn JSON Schema
[![Maven Central](https://img.shields.io/maven-central/v/no.ks.fiks/innsyn-json-schema)](https://search.maven.org/artifact/no.ks.fiks/innsyn-json-schema)
![GitHub](https://img.shields.io/github/license/ks-no/fiks-innsyn-json-schema)

Dette repoet inneholder JSON Schema-definisjoner for bruk mot indekseringstjenesten til Fiks Innsyn.

## Generering av modeller

Maven-artefakt med ferdig genererte POJO-klasser finnes på Maven Central:
```
<dependency>
    <groupId>no.ks.fiks</groupId>
    <artifactId>innsyn-json-schema</artifactId>
    <version>x.x.x</version>
</dependency>
```

For de som ønsker å generere modellklasser selv bør det bemerkes at det er brukt et custom format for 64-bits heltall, som ser slik ut: 
```
{
  "$id": "https://api.fiks.ks.no/innsyn/schema/types/int64.json",
  "$schema": "https://json-schema.org/draft/2019-09/schema",
  "title": "Int64",
  "description": "64-bits integer",
  "type": "integer",
  "format": "int64",
  "minimum": -9223372036854775808,
  "maximum": 9223372036854775807
}
```
int64-formatet er ikke definert i JSON Schema speccen, så dette må eventuelt konfigureres i verktøyet som brukes for generering.
