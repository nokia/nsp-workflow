![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## NFMP Port Configuration

### Description
This workflow is demoing port configuration using NFMP. It will search all ports network-wide matching a certain description (selector) and changes the administrative state and encapType. If the workflow runs into an error for any of the selected ports, it will rollback the complete campaign for all given ports.

### Version
NFMP Port Configuration - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
|   1.0 |  SW  |2019-02-14|first version|

### Prerequisites
Nokia NSP with Workflow Manager and NFMP

### Tested with
* Nokia NSP 18.12
* Nokia 7750SR running SR OS 16.0.R5 (CLASSIC MODE)

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage
The workflow can be initiated either via the WFM GUI or via the workflow management REST API

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
