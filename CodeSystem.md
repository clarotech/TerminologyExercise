# Examples for CodeSystems

For the demo I have created a CodeSystem based on a CareConnect one

Its Canonical URL is https://fhir.interopendemo/Demo-HumanLanguage

## Locate a CodeSystem via URL

```HTTP
GET {url}/CodeSystem?url={value}
```

## $lookup for a valid code in a CodeSystem
```HTTP
GET {url}/CodeSystem/$lookup?system=https://fhir.interopendemo/Demo-HumanLanguage&code=fi
```

## $lookup for an invalid code in a CodeSystem

This will not work as the CodeSystem declares itself to be case sensitive

```HTTP
GET {url}/CodeSystem/$lookup?system=https://fhir.interopendemo/Demo-HumanLanguage&code=FI
```

## $lookup for a SNOMED concept 

Concept Ids only - no description ids

```HTTP
GET {url}/CodeSystem/$lookup?system=http://snomed.info/sct&code=130987000
```

## $validate-code with no display

Concept Ids only - no description ids

```HTTP
GET {url}/CodeSystem/$lookup?system=http://snomed.info/sct&code=130987000
```
