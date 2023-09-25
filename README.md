# nobel-prize
This repository hosts the Nobel Prize app, the purpose of which is to enable search, exploration and discoverability of the information related to the awarded Nobel Prizes and Laureates. The Nobel Prize app makes use of two data sources: 
* the [Nobel Prize bundle](https://github.com/metaphacts/nobel-prize-bundle) built by [metaphacts GmbH](https://metaphacts.com/) from the data published by the [Nobel Prize Foundation](https://www.nobelprize.org/the-nobel-prize-organisation/the-nobel-foundation/);
* [wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), which SPARQL endpoint is queried in the runtime to enrich information about entities of the Nobel Prize bundle. 

# Live Demo
To showcase how [metaphactory](https://metaphacts.com/product) platform can deliver smooth and convenient end-user interaction on top of knowledge graphs, the Nobel Prize app has been published as a live demo: https://nobelprize.metaphacts.cloud/resource/StartPage.
# Nobel Prize App Deployment
install it through the *Apps administration* UI of your metaphactory instance.

To complete the installation a restart of the platform is required.

See https://help.metaphacts.com/resource/Help:AppDeployment for details on the deployment.

Notes:
we recommend to deploy the app in a fresh metaphactory installation

# Feedback
If you have any feedback about the live demo or the templates published in this repository, please reach out to dp@metaphacts.com. 
