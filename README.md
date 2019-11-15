# Fiks Innsyn JSON Schema

Dette repoet inneholder JSON Schema-definisjoner for bruk mot indekseringstjenesten til Fiks Innsyn.

## Generering av modeller

For Java-brukere kan Maven-artefakt med ferdig genererte POJO-klasser finnes på Maven Central:
```
    <groupId>no.ks.fiks</groupId>
    <artifactId>innsyn-json-schema</artifactId>
    <version>1.0.0</version>
```

For de som ønsker å generere modellene selv bør det bemerkes at vi har brukt et custom format for 64-bits heltall, som ser slik ut: 
```
{
  "type": [
    "string",
    "integer"
  ],
  "format": "int64"
}
```
int64-formatet er ikke definert i JSON Schema speccen, så dette må eventuelt konfigureres i verktøyet som brukes for generering.
Felter av denne typen kan også sendes inn som strenger.