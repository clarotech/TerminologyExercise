# Examples for ValueSets

For the demo I have created two ValueSets based on a CareConnect ones

Canonical URLs are
  * https://fhir.interopendemo/Allergy-Severity
  * https://fhir.interopendemo/Allergy-Severity-v2
  * https://fhir.interopendemo/Allergy-Severity-v3

## Expand - https://fhir.interopendemo/Allergy-Severity (include with ECL)

```HTTP
GET {url}/ValueSet/$expand?url=https://fhir.interopendemo/Allergy-Severity
```

## Expand - https://fhir.interopendemo/Allergy-Severity-v2 (multiple include)

```HTTP
GET {url}/ValueSet/$expand?url=https://fhir.interopendemo/Allergy-Severity-v2
```

## Expand - https://fhir.interopendemo/Allergy-Severity-v3 (includes & exclude)

```HTTP
GET {url}/ValueSet/$expand?url=https://fhir.interopendemo/Allergy-Severity-v3
```

## Expand - https://fhir.interopendemo/Allergy-Severity using a filter

```HTTP
GET {url}/ValueSet/$expand?url=https://fhir.interopendemo/Allergy-Severity&filter=Severe
```
