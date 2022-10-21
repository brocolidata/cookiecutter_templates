# dbt packages Cookiecutter Template

This template contains the code to create a `dbt_packages` like the examples in [brocolidata/dbt_packages](https://github.com/brocolidata/dbt_packages).


## How to use this cookiecutter
```
cookiecutter https://github.com/brocolidata/cookiecutter_templates.git \
    --directory="sample_dbt_package" \
    --output-dir .
```


## Inputs

| Name                 | Description                     | Required | Default Value    |
|----------------------|---------------------------------|----------|------------------|
| `long_project_name`  | Long name for your dbt project  | yes      | dbt_project_name |
| `short_project_name` | Short name for your dbt project | yes      | dbt              |
| `profile_name`        | Name of the default dbt profile  | no       | my-bigquery-db   |
| `target`             | Name of the default target      | no       | prod             |
