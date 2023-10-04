# nobel-prize
This repository hosts the *Nobel Prize app*, which enables search, exploration and discoverability of awarded Nobel Prizes and Laureates. The Nobel Prize app makes use of two data sources:
* The [Nobel Prize bundle](https://github.com/metaphacts/nobel-prize-bundle) built by [metaphacts](https://metaphacts.com/) from the data published by the [Nobel Prize Foundation](https://www.nobelprize.org/the-nobel-prize-organisation/the-nobel-foundation/);
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

# Feedback
If you have any feedback about the live demo or the apps published in this repository, please reach out to info@metaphacts.com. 
