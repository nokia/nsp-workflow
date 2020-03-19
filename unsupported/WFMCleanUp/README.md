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
|   1.0 |  SW  |2019-06-17|NSP19.6 updates|

### Prerequisites
Nokia NSP with Workflow Manager

### Tested with
* Nokia NSP 19.6

### Installation
Workflow can directly be imported/updated from GitHub using the WFM WebUI.

### Usage
By default NSP WFM removes all workflow execution results older than 120 days. In environment where WFM is regularly used, this causes a lot of execution results (workflow, task and action execution results) to be stored which impacts database size, performance and usability. This workflow helps to cleanup the execution history based on user-defined rules. The workflow can be scheduled to automatically clean-up the execution history.

If none of the attributes are provided, ALL workflow execution results will be removed. If one or more attributes are provided, these act as filter (logical AND) to only remove some results. `deleteBefore` allows the operator to specify a timestamps (date/time), so that all executions results from before are removed. In a similar way, the `deleteAge` defines the maximum age of execution results - while everything older than this will be removed from the database. The age is defined in seconds. With `workFlowName` one can limit the delete operation to a specific workflow. With `workFlowState` one can limit deletes to a specific result (SUCCESS, ERROR).

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
