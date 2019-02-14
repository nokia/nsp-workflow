![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## IBN Migrate PBB ELINE

### Description
This workflow will migrate an ELINE service from one B-VPLS to another.

### Version
IBN Migrate PBB ELINE - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
|   1.0 |  SW  |2019-02-14|first version|

### Prerequisites
Nokia NSP with Workflow Manager and IBN
IBN must have the intent for PBB ELINE installed

### Tested with
* Nokia NSP 18.12
* Nokia 7750SR running SR OS 16.0.R5 (MD MODE)

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage
The workflow can be initiated either via the WFM GUI or via the workflow management REST API

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
