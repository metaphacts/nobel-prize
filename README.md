# nobel-prize
This repository hosts the *Nobel Prize app*, which enables search, exploration and discoverability of awarded Nobel Prizes and Laureates. The Nobel Prize app makes use of two data sources:
* The [Nobel Prize bundle](https://metaphacts-datasets.s3.amazonaws.com/nobel-prize-bundle.trig.gz) built by [metaphacts](https://metaphacts.com/) from the data published by the [Nobel Prize Foundation](https://www.nobelprize.org/the-nobel-prize-organisation/the-nobel-foundation/);
* [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), whose SPARQL endpoint is queried in the runtime to enrich information about entities of the Nobel Prize bundle.

Besides the *Nobel Prize app*, the related *Nobel Prize branding app* is also hosted here. The *Nobel Prize branding app* contains style adjustments that override metaphactory's defaults to customize the look and feel of particular components. 

The main purpose of publishing the source code of these two apps was to show by example how interactive and smooth end-user apps can be built on top of low-code [metaphactory](https://metaphacts.com/produc) platform. Once you deploy the apps on your instance of metaphactory, you'll be able to peak inside the page templates to understand how metaphactory components work and tweak them for your usecase.  

# Live Demo
An instance of metaphactory with two apps comprise the Nobel Prize live demo: https://nobelprize.metaphacts.cloud.
The demo showcases metpahactory's ability to deliver a smooth user interface for exploration and discoveries on top of a Knowledge Graph. 
# Nobel Prize App Deployment
You can install both apps through the *Apps administration* UI of your metaphactory instance. The order, in which the apps are deployed, in this case, does not affect the result. 

To complete the installation, a restart of the platform is required.

See [https://help.metaphacts.com/resource/Help:AppDeployment](https://help.metaphacts.com/resource/Help:AppDeployment#uploading-zip-artifcat) for details on the deployment.

Notes:
* We recommend deploying the app in a fresh metaphactory installation.
* To obtain a copy of metaphactory you can start your [free trial](https://metaphacts.com/get-started) (Docker-based trial or trial on AWS marketplace are most suitable options).   
# Nobel Prize bundle
Please note that the bundle was created by metaphacts GmbH solely for exploration and demonstration purposes. 

Neither the bundle nor metaphacts are associated with the Nobel Prize Foundation and its website.

The Nobel Prize bundle can be downloaded at: https://metaphacts-datasets.s3.amazonaws.com/nobel-prize-bundle.trig.gz
## What is in the bundle 
* The original data dump 'nobel-prize-dataset.trig' was retrieved and cached from https://data.nobelprize.org/sparql
* `nobel-prize-dataset-place-hierachy-extension.trig` was created as an extension by metaphacts taking `nobel-prize-dataset.trig` as input. The place hierarchy has been constructed utilizing the knowledge within the data and with the help of federation to wikidata/dbpedia.
* `nobel-prize-metaphacts-shacl-ontology.trig` was created by metaphacts based on the original nobel prize ontology [published](https://data.nobelprize.org/specification/) by the Nobel Prize Foundation.
* `nobel-prize-metaphacts-skos-vocabulary.trig` was created by metaphacts to handle the vocabulary terms within metaphactory. The identifiers of the "category" individuals from the official Nobel Prize OWL ontology have been reused and turned into a vocabulary (defined as SKOS scheme). The terms also have been augmented and enriched with additional structure and metadata solely for exploration and demonstration purpose.
## License
For the original nobel prize data the official license and terms of usage apply, i.e. please refer to https://data.nobelprize.org/specification/ and https://www.nobelprize.org/about/terms-of-use-for-api-nobelprize-org-and-data-nobelprize-org/ .
# How to reproduce the Nobel Prize demo on your instance of metaphactory
1. Deploy an instance of metaphactory (you can start your trial and obtain a copy of metaphactory [here](https://metaphacts.com/get-started).
2. Deploy nobel prize apps - see the *Nobel Prize App Deployment* section above.
3. Load the Nobel Prize bundle from the S3 bucket by clicking "SPARQL" link in the application header of your metaphactory instance and then pasting and running the following command:
`LOAD <https://metaphacts-datasets.s3.amazonaws.com/nobel-prize-bundle.trig.gz>`.
# Feedback
If you have any feedback about the live demo or the apps published in this repository, please reach out to info@metaphacts.com. 
