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
2. Create a repository (ID: data-night, Region: europe-west1)
3. Link repository to [github](https://github.com/devoteamgcloud/data-night-dataform)
* In github: Copy the clone link
* In Dataform: Launch your repo, Go to "Settings" tab.
* Click on "Connect with Git"
* Paste the copied link (Github repo Url)
* Default branch name "main"
* Enter Secret Resource ID: `projects/376282389739/secrets/dataform-github-access`
4. Create a workspace (ID: [your-project-id]) *-equivalent to personal branch as well-*
5. Adjust dataform.json
6. Confirm & Apply transformations  (sql statements in Dataform)
7. View the execution details (pops up at the bottom once you run the workflow)
8. Go to SQL Workspace tab of the BigQuery (left pane)
9. View the new dataset & tables in Bigquery `ML-house-prices`
10. Analyze in Looker Studio *optional*
11. 
