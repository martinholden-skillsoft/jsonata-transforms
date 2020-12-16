# successfactors-force-locale-transform

## Description
This transform uses the Percipio JSONata library of functions, and configuration methods.

The transform is based on the default successfactors transform and configuration.

The transform allows a specific Locale to be specified for ALL input records, the use case would be to generate second ITEM_DATA file to update localisations for content.

The transform clones the $ context, the input record, and modifies it so that:

* The localeCodes array is a 1 element array and the value will be the value of the $forceLocale variable
* The localizedMetadata array is a 1 element array and the value will be either:
  * The localizedMetadata array element that matches the $forceLocale
  * The first element (i.e. default) of the localizedMetadata array, but with its 'localeCode' set to $forceLocale

This means that we can then use the standard transform but we change the context so instead of:

```
$transformed_data :=
  $.{
```

We use our cloned object $forceLocaleRow

```
$transformed_data :=
  $forceLocaleRow.{
```

This means that in our standard transform functions $ does not refer to the JSON we got from percipio as input, but our clone of this.
