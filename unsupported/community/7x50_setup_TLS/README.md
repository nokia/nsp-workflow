![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# NSP WFM Demo
## 7x50 Setup TLS

### Description
This workflow will generate all the certificates required to enable TLS on a
Nokia 7x50 router. The certificates will be copied to the node along along the
necessary configuration to enable TLS.

If certificates have been created before, hostkey and hostcert will be
reissued, copied and installed. This is used to rollout updated certs
to replace the existing ones before expiration.

### Version
7x50 Setup TLS - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
|   1.0 |  SW  |2019-09-06|             |

### Prerequisites
Nokia NSP with Workflow Manager

### Installation
Workflow can be imported directly from GitHub. WebUI form JSON must be manually
be imported. There is a workflow action to setup the environment for that
workflow, which needs to be imported and adjusted.

### Usage
Coming soon!

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md)
file for details.
