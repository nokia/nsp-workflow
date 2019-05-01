![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## 7x50 Setup Telemetry

### Description
This workflow will generate all the certificates required to enable the
telemetry TLS on a Nokia SR OS device. The certificates will be copied
to the node along along the necessary configuration to enable TLS.

If certificates have been created before, hostkey and hostcert will be
reissued, copied and installed. This is used to rollout updated certs
to replace the existing ones before expiration.

### Version
7x50 Setup Telemetry - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
|   1.0 |  SW  |2019-05-01|first version|

### Prerequisites
Nokia NSP with Workflow Manager and Telemetry

### Tested with
* Nokia NSP 19.3
* Nokia 7750SR running SR OS 16.0.R7 (CLASSIC MODE)

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
