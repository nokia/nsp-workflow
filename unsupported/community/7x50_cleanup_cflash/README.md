![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP WFM demo workflow
## Workflow Manager - Cleanup CF

### Description

### Version
7x50 Cleanup CF - version 1.0.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
| 1.0.0 |  SW  |2019-09-06|first version|

### Prerequisites
Nokia NSP with Workflow Manager

### Tested with
* Nokia NSP 19.6

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage
The operator must fill-in `neId`, `dir` and `deleteAge` attributes to call the workflow. `deleteAge` defines the maximum age, while everything older will be removed from the filesystem. The age is defined in seconds. The `dryRun` can be used to preview the files to be deleted, without actually
deleting the files. The `concurrency` defines, how many files would be deleted in parallel.

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
