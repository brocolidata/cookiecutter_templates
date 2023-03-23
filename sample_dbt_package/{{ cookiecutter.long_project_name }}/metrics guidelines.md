# DBT METRICS GUIDELINES

## Introduction

This document presents guidelines on how to use "metrics" with dbt.

Please refer to the following link that provides a first set of suggestions on how to organize and use metrics within a dbt project ( https://docs.getdbt.com/blog/how-to-design-and-structure-metrics#when-to-put-business-logic-in-the-semantic-layer-vs-the-modeling-layer )

Metrics are a major component of the dbt Semantic layer. We first need to define a metric and how we want it to act then we need to query the metric for it to give us back a result.


## Metrics definition

The metrics folder will hold all the metrics definitions per domain in a .yml file.

We recommend:
creating the metrics folder within ODS
creating a metrics folder per Business Domain
creating one .yml file per Business Domain
keeping logic in the modeling layer ->  avoid complex logic in the metrics definition
curating dimensions -> do not include ALL the columns as most models contain columns irrelevant for end-user analysis


## Metrics querying

Metrics querying is performed through the Calculate macro.

We recommend:
querying metrics within PRS
querying models for end-user analysis  -> avoid querying to create intermediate models that have no analysis purpose
only using the secondary calculations that are needed -> avoid unnecessary secondary calculations
keeping logic in the metrics definition as much as possible. However, sometimes logic needs to be used on top of your query.

## Links and references

How to design and structure dbt metrics: Recommendations for getting started - https://docs.getdbt.com/blog/how-to-design-and-structure-metrics#when-to-put-business-logic-in-the-semantic-layer-vs-the-modeling-layer

dbt hub metrics (defintion, available calculations and querying) - https://hub.getdbt.com/dbt-labs/metrics/latest/

dbt metrics official documentation - https://docs.getdbt.com/docs/build/metrics
