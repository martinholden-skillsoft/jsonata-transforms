# collections-transform

## IMPORTANT
As at December 2020 the Percipio backend code will not support multiple outputs for single input, and so this code whilst it will work in the [JSONata Percipio Excerciser](https://martinholden-skillsoft.github.io/jsonata-percipio-exerciser/build/) will not workas a Percipio Scheduled Job

## Description
This transform illustrates how to create multiple outputs from a single input

The transform takes the Percipio JSON list of "collections" and groups them into chunks of 3, controlled by $collectionMaxColumns in the transform.

So as example if item has 10 collections, we will get 4 records for each input record.

First record has Collections 1,2,3, next has 4,5,6 etc

