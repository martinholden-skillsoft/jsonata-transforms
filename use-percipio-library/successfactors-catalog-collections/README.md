# successfactors-catalog-collections-transform

## IMPORTANT
As at December 2020 the Percipio backend code will not support multiple outputs for single input, and so this code whilst it will work in the [JSONata Percipio Excerciser](https://martinholden-skillsoft.github.io/jsonata-percipio-exerciser/build/) will not workas a Percipio Scheduled Job

## Description
This transform uses the Percipio JSONata library of functions, and configuration methods.

The transform is based on the default successfactors transform and configuration.

The transform allows the collection information included in the Percipio metadata to be used to populate SuccessFactors CATALOG_1 thru CATALOG_3 columns.

The transform if the input item has 10 collections, we will generate 4 records for each input record.

First record has Collections 1,2,3, next has 4,5,6 etc

The transform also has a new config option:

```
"includeDefaultCatalog" : false
```

This if set includes the config $catalog value in the list.


