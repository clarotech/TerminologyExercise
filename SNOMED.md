# Examples for SNOMED Intrinsic ValueSets

Caution - The SNOMED version on the server is not up to date.

## Subsumption (Blood Pressure)

```HTTP
GET {url}/ValueSet/$expand?url=http://snomed.info/sct?fhir_vs=isa/75367002
```

## List published RefSets

```HTTP
GET {url}/ValueSet/$expand?url=http://snomed.info/sct?fhir_vs=refset
```


## Expand specific RefSet

```HTTP
GET {url}/ValueSet/$expand?url=http://snomed.info/sct?fhir_vs=refset/734139008
```
