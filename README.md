# WELCOME TO DATA NIGHT
Dataform project repository designed for Data Night - Feb 2023
![data-night](https://github.com/devoteamgcloud/data-night-dataform/blob/main/pics/data-night.jpg)

This document contains instructions to process house-prices data, analyze & prepare for Machine Learning session.
House & Sales data are in bigquery. 
## Objectives
:dart: Access to DataForm repository in github \
:dart: Extract data from Bigquery project \
:dart: Apply transformations through DataForm service & Load into personal project Bigquery \
:dart: (optional) Analyze through Looker Studio 

## Steps
1. Go to Bigquery -> Dataform in console
2. Create a repository (ID: data-night, Region: europe-west1)
3. Click & launch the repository
4. Link repository to [github](https://github.com/devoteamgcloud/data-night-dataform):
* 4.1. In github: Copy the [clone link](https://github.com/devoteamgcloud/data-night-dataform.git)
* 4.2. In Dataform: Launch your repo, Go to **Settings** tab.
* 4.3. Click on **Connect with Git**
* 4.4. Paste the copied link (Github repo Url)
* 4.5. Default branch name `main`
* 4.6. Enter Secret Resource ID: `projects/376282389739/secrets/dataform-github-access
5. Go to **Development Workspaces** tab in your repo
6. Create a workspace (ID: [your-project-id]) *-equivalent to personal branch as well-*
7. Click & launch the workspace
8. Verify the project structure as shown:

![image](https://github.com/devoteamgcloud/data-night-dataform/blob/main/pics/folder-structure.jpg?raw=true)

9. Adjust dataform.json file (enter your project id)
10. Review the transformations
11. Apply transformations  (sql statements in Dataform) through **Start Execution** button - *All actions*
12. View the execution details (pops up at the bottom once you run the workflow)
13. Go to SQL Workspace tab of the BigQuery (left pane)
14. View the new dataset & tables in Bigquery `ML-house-prices`
15. (Optional) We should convert some fields from string to numeric data-types:
* 15.1. Here is a sql statement that casts a field as integer, then converts feet square into meter square:
```
js { function convert_feet_square_to_meter(field) {
    return `
    cast (${field} as integer) * 0.092903 as ${field}
    `;
}
}
```
* 15.2. Copy this function into definitions/transformations/training_house_sales.sqlx **Before the sql statements (ie. after line 15)** as a macro
* 15.3. Call the function within *training_casted* statement. Example:
`${convert_feet_square_to_meter("LotFrontage")},
${convert_feet_square_to_meter("MasVnrArea")}`
* 15.4. If it's compiled successfully, reexecute the 

16. (Optional) Analyze in Looker Studio:
* 16.1. Find the ML_house_prices.training_set table in Bigquery sql workspace & click
* 16.2. Click on **Export** then Explore with Looker Studio
* 16.3. Try to visualize the data

## Scenario Review
![scenario](https://github.com/devoteamgcloud/data-night-dataform/blob/main/pics/scenario.jpg)