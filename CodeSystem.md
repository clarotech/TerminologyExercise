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

## $validate-code with no display - valid

```HTTP
GET {url}/CodeSystem/$validate-code?url=https://fhir.interopendemo/Demo-HumanLanguage&code=fr
```


## $validate-code with no display - invalid

Invalid Upper Case

```HTTP
GET {url}/CodeSystem/$validate-code?url=https://fhir.interopendemo/Demo-HumanLanguage&code=FR
```

## $validate-code with code & display - valid

```HTTP
GET {url}/CodeSystem/$validate-code?url=https://fhir.interopendemo/Demo-HumanLanguage&code=ru&display=Russian
```


## $validate-code with code & display - invalid

Invalid code/display combination

```HTTP
GET {url}/CodeSystem/$validate-code?url=https://fhir.interopendemo/Demo-HumanLanguage&code=ru&display=German
```

## $validate-code SNOMED with preferred term

Invalid code/display combination

```HTTP
GET {url}/CodeSystem/$validate-code?url=http://snomed.info/sct&code=22298006&display=Myocardial infarction
```

## $validate-code SNOMED with synonym

Invalid code/display combination

```HTTP
GET {url}/CodeSystem/$validate-code?url=http://snomed.info/sct&code=22298006&display=Heart attack
```
