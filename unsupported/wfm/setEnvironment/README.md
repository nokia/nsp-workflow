![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## Workflow Manager - Set Environment

### Description
Signed workflows cannot be modified without breaking the signature. To achieve
portability of workflows without the need to modify workflows after imported
to a system, it is desired to have environment specific needs stored outside
the workflow. As in NSP19.6 WFM has no common environment feature, this
workflow creates a Mistral action called 'environment' that can be called
by various workflows to load the environment settings. This workflow is
used to setup the environment including all variables that are used by the
WFM examples found on GitHub.

### Version
WFM Set Environment - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author| Date       |Comments         |
|-------|------|------------|-----------------|
|   1.0 |  SW  | 2019-08-06 |Initial version  |

### Prerequisites
Nokia NSP with Workflow Manager

### Tested with
* Nokia NSP 19.6

### Installation
Workflow can directly be imported/updated from GitHub using the WFM WebUI.

### Usage
Call the workflow once to initially setup you WFM environment. It will create
an action called 'environment', that stores environmental settings such as
servers, usernames and passwords to be used. Make sure to modify all values
to fit your environment.

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md)
file for details.
