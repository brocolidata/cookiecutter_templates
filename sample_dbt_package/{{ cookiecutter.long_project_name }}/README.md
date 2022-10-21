# {{ cookiecutter.long_project_name }} dbt project

## dbt project structure
```
── {{ cookiecutter.long_project_name }}                        
    ├── README.md
    ├── analysis               # 
    ├── dbt_packages           #
    ├── dbt_project.yml        # main settings file
    ├── logs
    ├── macros                 #                  
    ├── models                 # models and sources ( .sql, .yml)
    ├── packages.yml           # additional dbt packages
    ├── target                 # compiled files
    └── tests                  # data tests
```



## Basic local dbt usage:

1. Check if the project is valid by running `dbt debug`
2. Install dependencies (specified in *packages.yml*) by running `dbt deps`
3. Follow instructions to generate the content of *stg.yml* in order to define the sources of your future models
4. Follow instructions to Stage sources defined in *stg.yml*
5. In */models*, write SQL queries inside `.sql` scripts to create your tables from sources or other tables *(optionally, you can add documentation to your tables and sources in **.yml** files)* 
6. See [dbt docs instructions](https://docs.getdbt.com/reference/node-selection/syntax)