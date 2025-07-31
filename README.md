# mule-scripting

A collection of scripts for automating and simplifying various things in Mulesoft.

## dependencies
* [Anypoint CLI](https://docs.mulesoft.com/anypoint-cli/latest/)
* [jq](https://jqlang.org/)

  If bc isn't installed **Google** `bc linux install`
  
## scripts/vcore

The `scripts/vcore` script is used to sum the vCore for each app in use in an Environment * the number of workers for that app. It produces total vCore usage for an Environment and the total use for all Environments.
  
### *sample output*
🔎 Environment: QA
  Total vCore used in QA: 0


=============================

🧮 Total vCore across all environments: 42.0

## scripts/vcore-lg

To identify large vCore consumers, run `scripts/vcore-lg`. The script iterates over Environments and reports vCore usage at or above the Default setting of 0.3 vCore. You can override the default by using the command line switch `-c 0.4 or --cpu 0.4`.

### *sample output*
./vcore-lg 
🔍 Listing CloudHub apps using ≥ 0.3 vCores
=======================================================

🌐 Environment: Dev

🌐 Environment: QA
  hello-world-qa: 3 vCores
  party-time-qa: 42 vCores

