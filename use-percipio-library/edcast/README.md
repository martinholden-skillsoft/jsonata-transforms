# edcast-transform

## Description
This transform uses the Percipio JSONata library of functions, and configuration methods.


edcast_config.json
This is a "custom config" JSON object, that contains the mapping between Percipio locales and EdCast locales, plus config for title etc

edcast.jsonata
This is a transform that uses the "custom config" but also a number of the standard functions and the Saba Keywords function.

The transform is based on an example by Greg Breeden, and so for example "cleans" the description by removing bad characters that EdCast doesnt like, plus encoding CR/LF etc