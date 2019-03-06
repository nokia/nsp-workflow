![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## Workflow Manager - Cleanup Executions

### Description

### Version
WFM Cleanup Executions - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
|   1.0 |  ML  |2019-01-28|first version|
|   1.1 |  SW  |2019-03-05|usability improvements|


### Prerequisites
Nokia NSP with Workflow Manager

### Tested with
* Nokia NSP 18.12

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage
The operator must fill-in `token_auth` and `rest_gateway_host` to call the workflow. The other four attributes are optional to provide and have the following functionality.
If none of the attributes are provided, ALL workflow execution results will be removed. If one or more attributes are provided, these act as filter (logical AND) to only remove some results.
`fromDate` allows the operator to specify a timestamps (date/time), so that all executions results from before are removed. In a similar way, the `byAge` defines the maximum age of an execution result - while everything older will be removed from the database. The `byAge` attributes gets priority over the `fromData` if both attributes are provided. The age is defined in seconds.
With `workFlowName` one can limit the delete operation to a specific worklow. With `workFlowState` one can limit deletes to a specific result (SUCCESS, ERROR).

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
