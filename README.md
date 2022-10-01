# ontologies
This repo contains the Ontologies being developed by the [KnACC](https://knacc.umbc.edu) team.
All ontologies are available at our [API endpoint](http://knacc1.rs.umbc.edu/api/graphiql)

## 🦉 OWL  
Available in the `owl` directory and include:
- `enc_100k.owl` - Encrypted patient data.  
- `test_result.owl` - Ontology for Synthea data. 

## ✨ SPARQL queries 
Available in the `SPARQL` directory and include:
- `get_patients_enc_100k.rq` - queries the encrypted data.
- `get_patients_test_result.rq` - queries the Synthea data. 

## 🐶 Example API queries
The [API endpoint](http://knacc1.rs.umbc.edu/api/graphiql) run SPARQL queries listed above and fetch patient data as an electronic health record. Example queries:
```
query encryptedData {
  encryptedEhrs {
                individual
                diagnoses
               }
}
```

```
query syntheticData {
  syntheticEhrs {
                individual
                diagnoses
               }
}
```