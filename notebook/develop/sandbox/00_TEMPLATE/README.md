# GA4 API

## Initial setup

1. Copy "template" file to your user folder in notebook sendbox(example PATH to user folder /notebook/develop/sandbox/###, where ### is your name) 
2. Make sure that you have config folder under your user, if no please download from [martech-config-bucket](https://console.cloud.google.com/storage/browser/martech-config-bucket;tab=objects?forceOnBucketsSortingFiltering=true&project=katia-playground) config folder 
(martech-config-bucket > gcp) and add config folder to your user folder in notebook sendbox(example PATH to user folder /notebook/develop/sandbox/###, where ### is your name) 

## Prepare input file
### Custom dimentions 
1) You need to update "input_file.xlsx" (sheet "Tabelle1") and list there custom dimensions that need to be created. There are 4 columns in the sheet:
- "displayName" - a unique name for the dimension;
- "parameterName" - an item parameter when you choose the Item scope or an event parameter when you choose the Event scope or a user property when you choose the User scope;
- "scope" - specifies to which data the custom dimension or metric will be applied; there are 3 possible values: "EVENT" for an event-scoped dimension, "USER" for a user-scoped dimensio and "ITEM" for an item-scoped dimension;
- "description" - an optional text used to identify a custom dimension;
![Alt text](/pix/cdcreate.png)

2) You need to update "input_file.xlsx" (sheet "Tabelle2") and list there GA4 property IDs for which custom dimensions listed in sheet "Tabelle1" need to be created. There is 1 column in the sheet with header "property_id"

### Audienced
1) configure in one GA4 property audiences manualy, it would be used as template for another properties
2) important to add description to all audiences, as without it api wouldn't run



