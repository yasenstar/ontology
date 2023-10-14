# Ontology: MyKnowledgeNetwork

```SPARQL
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX kg: <http://www.semanticweb.org/v0cn037/ontologies/2023/9/MyKN#>

SELECT ?tool ?company ?date ?comment
WHERE {
    ?company kg:adopting ?tool .
    ?company rdfs:comment ?comment .
    ?company kg:dateUseArchi ?date .
    ?tool rdfs:label "Archi"
    filter ( datatype(?comment) = xds:string ) .
}
ORDER BY ?date
```