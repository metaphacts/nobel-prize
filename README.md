# nobel-prize
This repository hosts the *Nobel Prize app*, which enables search, exploration and discoverability of awarded Nobel Prizes and Laureates. The Nobel Prize app makes use of two data sources:
* The [Nobel Prize bundle](https://metaphacts-datasets.s3.amazonaws.com/nobel-prize-bundle.trig.gz) built by [metaphacts](https://metaphacts.com/) from the data published by the [Nobel Prize Foundation](https://www.nobelprize.org/the-nobel-prize-organisation/the-nobel-foundation/);
* [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), whose SPARQL endpoint is queried in the runtime to enrich information about entities of the Nobel Prize bundle.

Besides the *Nobel Prize app*, the related *Nobel Prize branding app* is also hosted here. The *Nobel Prize branding app* contains style adjustement that override metaphactory's defaults to customize the look and feel of particular components. 

# Live Demo
To showcase how [metaphactory](https://metaphacts.com/product) can deliver a smooth and intuitive end-user interaction on top of knowledge graphs, the *Nobel Prize app* together with the *Nobel Prize branding app* have been published as a live demo: https://nobelprize.metaphacts.cloud.
# Nobel Prize App Deployment
You can install both apps through the *Apps administration* UI of your metaphactory instance. The order, in which the apps are deployed, in this case, does not affect the result. 

To complete the installation, a restart of the platform is required.

See [https://help.metaphacts.com/resource/Help:AppDeployment](https://help.metaphacts.com/resource/Help:AppDeployment#uploading-zip-artifcat) for details on the deployment.

Notes:
We recommend deploying the app in a fresh metaphactory installation. 
# Nobel Prize bundle
Please note that the bundle was created by metaphacts GmbH solely for exploration and demonstration purpose. 

Niether the bundle nor metaphacts are associated with the Nobel Prize Foundation and its website.
## What is in the bundle 
* The original data dump 'nobel-prize-dataset.trig' was retrieved and cached from https://data.nobelprize.org/sparql
* `nobel-prize-dataset-place-hierachy-extension.trig` was created as an extension by metaphacts taking `nobel-prize-dataset.trig` as input. The place hierarchy has been constructed utilizing the knowledge within the data and with the help of federation to wikidata/dbpedia.
* `nobel-prize-metaphacts-shacl-ontology.trig` was created by metaphacts based on the original nobel prize ontology [published](https://data.nobelprize.org/specification/) by the Nobel Prize Foundation.
* `nobel-prize-metaphacts-skos-vocabulary.trig` was created by metaphacts to handle the vocabulary terms within metaphactory. The identifiers of the "category" individuals from the official Nobel Prize OWL ontology have been reused and turned into a vocabulary (defined as SKOS scheme). The terms also have been augmented and enriched with additional structure and metadata solely for exploration and demonstration purpose.
## License
For the original nobel prize data the official license and terms of usage apply, i.e. please refer to https://data.nobelprize.org/specification/ and https://www.nobelprize.org/about/terms-of-use-for-api-nobelprize-org-and-data-nobelprize-org/ .
# Feedback
If you have any feedback about the live demo or the apps published in this repository, please reach out to info@metaphacts.com. 
