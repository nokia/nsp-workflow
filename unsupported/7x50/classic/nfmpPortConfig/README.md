![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## NFMP Port Configuration

### Description
This workflow is demoing port configuration using NFMP. It will search all ports network-wide matching a certain description and changes the admin-state, mode and encapsulation type. The workflow has an option to rollback on error - to restore the configuration for all given ports when it runs into an error for any of the selected ports.

### Version
NFMP Port Configuration - version 1.0.1

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
| 1.0.0 |  SW  |2019-02-14|first version|
| 1.0.1 |  SW  |2019-08-21|updated for nsp19.6|

### Prerequisites
Nokia NSP with Workflow Manager and NFMP

### Tested with
* Nokia NSP 19.6-1
* Nokia 7750SR running SR OS 19.5.R2 (CLASSIC MODE)

### Installation
Import the workflow from GitHub and change from DRAFT to
RELEASED. Make sure, that the environment has been updated
to contain the Basic token to authenticate against NFM-P.

### Usage
The workflow can be initiated either via the WFM GUI or via the workflow management REST API

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
