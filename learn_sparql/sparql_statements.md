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

# query ex015

```SPARQL
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

PREFIX ls: <http://www.semanticweb.org/yasen/ontologies/2023/9/learnsparql#>

SELECT ?craigEmail
WHERE {
    ?person ls:firstName "Craig" .
    ?person ls:lastName "Ellis" .
    ?person ls:email ?craigEmail .
}
```

Result:

```
craigellis@yahoo.co^^xsd:string	
c.ellis@usairwaysgroup.com^^xsd:string
```

# filename: ex017

```SPARQL
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

PREFIX ls: <http://www.semanticweb.org/yasen/ontologies/2023/9/learnsparql#>

SELECT ?personFirstName ?personLastName
WHERE {
    ?person ls:homeTel "(209) 276-5135" .
    ?person ls:firstName ?personFirstName .
    ?person ls:lastName ?personLastName .
}
```

# ex019

```SPARQL
SELECT ?propertyValue
WHERE {
    ?person ls:firstName "Cindy" .
    ?person ls:lastName "Marshall" .
    ?person ls:email ?propertyValue .
}
```

Result:

```
cindym@gmail.com^^xsd:string
```

# ex021

```SPARQL
SELECT *
WHERE {
    ?s ls:email ?o .
    FILTER (regex(?o, "yahoo", "i"))
}
```

Note: you cannot have wild query of predicate in Snap SPARQL query within Protege, which is one functional bug.

Result:

|?s |         ?o |
| --- | --- |
|ls:craig	| craigellis@yahoo.co^^xsd:string |

# Figure 1-3

The `d:musicalArtist` should be just `d:artist`:

```SPARQL
PREFIX d: <http://dbpedia.org/ontology/>

SELECT ?artist ?album WHERE {
    ?album d:producer :Timbaland .
    ?album d:artist ?artist .
}
ORDER BY ?artist
```