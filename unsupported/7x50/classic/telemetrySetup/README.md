# Setup Telemetry Workflow Blueprint

Nokia NSP Workflow Manager Blueprint - Setup Telemetry Workflow

## Getting Started

This workflow will generate all the certificates required to enable gRPC telemetry collection on a Nokia SR.
The certificates will be copied to the SR along with  all necessary configuration to enable gRPC.
If the node has physical port 1/1/1 configured, the workflow will enable a 2 minute collection of telemetry data.

### Prerequisites

Nokia NSP with Workflow Manager and Telemetry

### Installing

Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

## Running the workflow

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


## Deployment

This is a sample workflow and should only be used for lab deployments. Additional work is required to enable the workflow to be used in a live system

## Tested with

* NSP 18.12
* 7750 SR 16.0 R5

## Versioning

This is version 1

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details



