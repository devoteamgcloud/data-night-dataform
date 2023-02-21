# WELCOME TO DATANIGHT
Dataform project repository designed for Data Night - Feb 2023

This document contains instructions to process house-prices data, analyze & prepare for Machnine Learning session.
House & Sales data are in bigquery. 
## Objectives
* Access to DataForm repository in github
* Extract data from Bigquery project
* Apply transformations through DataForm service & Load into personal project Bigquery
* (optional) Analyze through Looker Studio
* 
## Steps
1. Go to Bigquery -> Dataform in console
2. Create a repository (data-night, europe-west1)
3. Link repository to [github](https://github.com/devoteamgcloud/data-night-dataform)
* In github: Copy the clone link
* In Dataform: Launch your repo, Go to "Settings" tab.
* Click on "Connect with Git"
* Paste the copied link (Github repo Url)
* Default branch name "main"
* Enter Secret Resource ID: `projects/376282389739/secrets/dataform-github-access`
4. Create a workspace *(equivalent to personal branch as well)*
5. Adjust dataform.json
6. Confirm & Apply transformations  (sql statements in Dataform)
7. View the outcome in Bigquery
8. Analyze in Looker Studio
9. 


