![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP WFM demo workflow
## Workflow Manager - Cleanup CF

### Description

### Version
Cleanup CF - version 1.0.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
| 1.0.0 |  SW  |2019-05-13|first version|

### Prerequisites
Nokia NSP with Workflow Manager

### Tested with
* Nokia NSP 19.3

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage
The operator must fill-in `host`, `user`, `passwd` and `dirs` attributes to call the workflow. The other attributes are optional and have the following functionality:
`deleteBefore` allows the operator to specify a timestamps (date/time), so that all files from before are removed. In a similar way, the `deleteAge` defines the maximum age - while everything older will be removed from the filesystem. The age is defined in seconds.

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
