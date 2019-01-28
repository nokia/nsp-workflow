![NOKIA](https://raw.githubusercontent.com/nokia/nsp-workflow/master/logo.png)
# Nokia NSP Workflow Manager Blueprints
## 7x50 Setup Telemetry

### Description
This workflow will generate all the certificates required to enable the
telemetry API (using gRPC over TLS) on a Nokia SR OS device. The certificates
will be copied to the node along along the necessary configuration to enable
gNMI. If the node has physical port 1/1/1 configured, the workflow will enable
a 2 minute collection of telemetry data.

### Version
7x50 Setup Telemetry - version 1.0

### Support level
Unsupported, use at your own risk!

### History
|Version|Author|Date      |Comments     |
|-------|------|----------|-------------|
|   1.0 |  ML  |2019-01-28|first version|

### Prerequisites
Nokia NSP with Workflow Manager and Telemetry

### Tested with
* Nokia NSP 18.12
* Nokia 7750SR running SR OS 16.0.R5 (CLASSIC MODE)

### Installation
Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

### Usage
The workflow can be initiated either via the WFM GUI or via the workflow management REST API
The following parameters must be supplied

```
    "token_auth": The REST API Bearer token e.g. "YWRtaW46Tm9raWFOc3AxIQ==",
    "rest_gateway_host": The IP address of the NSP REST gateway e.g. "135.121.148.11",
    "rootUser": The user account to run the openssl commands e.g. "root",
    "rootPassword": The password for the rootUser e.g. "NokNsp1!",
    ftpHost: The IP address of the certificate host e.g. '192.168.96.10'
    ftpUser: The ftp user name to transfer the certificates e.g. 'root'
    ftpPassword: The ftp user password to transfer the certificates e.g.'NokNsp1!'
    "neIp": The management IP address of the SR e.g. "192.168.96.44",
    "neName": The node name of the SR e.g. "s168_96_44_Both",
    "neUser": The SR user account e.g. "admin",
    "nePassword": The SR user account password e.g. "admin",
    "cfLoc": The location of the SR compact flash e.g. "cf3"
```

Additionally, the workflow may be initiated via the workflow management REST API

```
POST /wfm/api/v1/execution HTTP/1.1

{
    "workflow_id": "b0ceb995-b126-4798-b1e6-82db9bcfc9f7",
    "input": {
        "token_auth": "YWRtaW46Tm9raWFOc3AxIQ==",
        "rest_gateway_host": "135.121.148.11",
        "rootUser": "root",
        "rootPassword": "NokNsp1!",
        "ftpHost": "192.168.96.10",
        "ftpUser": "root",
        "ftpPassword": "NokNsp1!",
        "neIp": "192.168.96.44",
        "neName": "s168_96_44_Both",
        "neUser": "admin",
        "nePassword": "admin",
        "cfLoc": "cf3"
    },
    "params": {},
    "output": {}
}
```

### License
This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details.
