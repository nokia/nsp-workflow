![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# NSP WFM Demo
## 7x50 Setup SSH users

### Description
This package contains a set of workflows to create and delete CLI/SSH users on Nokia SR OS devices. Key-based authentication is used.

### Version
1.0

### Workflows contained
| Workflow            | Usage                            |
|---------------------|----------------------------------|
| addUser             | creates SSH user on one node     |
| delUser             | removes SSH user from one nodes  |
| userMgmtCampaign    | add/delete SSH user on all nodes |
| cleanupUserCombined | deletes SSH user on all nodes    |

The userMgmtCampaign depends on the addUser and delUser workflows. It will
fetch the inventory and then run the required action for all 7x50 nodes.

The cleanupUserCombined shows an alternative, where the inventory lookup and
the actual execution are combined in the same workflow. Checking the execution
results one would see a single workflow execution, with a low amount of actions
but many tasks.

### Support level
Unsupported, use at your own risk!

### Prerequisites
None

### Tested with
* Nokia NSP 19.6
* Nokia SR OS 19.5.R1 (7750SR12 VSIM)

### Installation
Make sure, that an action is in place to set the environment to execute those
workflows. The environment is actually needed for server addresses and accounts
which could not be auto-resolved. The variables must be adapted to the local
environment the workflows are executed against.

Note: Environment actions are made for portability of workflows. It must be
avoided to hardcode those settings into individual workflows, while adapting
it to a NSP installation would break signatures and is a lot of duplication
of work. Trade-off needs to be made, to always ask the operator by making
those variables a workflow attribute. For the ease of use, operators would
complain always to enter that sort of additional data - while sometimes
they would even struggle to know what to enter.

| Environment Variable | Example Value | Usage                               |
|----------------------|---------------|-------------------------------------|
| wfmServer            | 192.168.0.10  | server to copy the SSH id from      |
| wfmUsername          | root          | username to login into the server   |
| wfmPassword          | changeme      | password to login into the server   |
| mdcServer            | localhost     | to resolve the API endpoint for MDC |
| mdcPort              | 8545          | to resolve the API endpoint for MDC |

### Usage
Coming soon!

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
