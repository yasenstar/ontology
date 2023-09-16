# query ex013

```SPARQL
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

PREFIX ls: <http://www.semanticweb.org/yasen/ontologies/2023/9/learnsparql#>

SELECT ?craigEmail
WHERE {
    ?person ls:firstName "Craig" .
    ?person ls:email ?craigEmail .
}
```