# Service Fulfillment Port Move Workflow Blueprint

Nokia NSP Workflow Manager Blueprint - Service Fulfillment Port Move Workflow

## Getting Started

This workflow will move all L2 and L3 services from one port to another. The ports may be in different NEs.

### Prerequisites

Nokia NSP with Workflow Manager and Service Fullfilment

### Installing

Download the workflow and then use the Workflow Manager workflow Import functionality to import the workflow into your WFM instance.

## Running the workflow

The workflow can be initiated either via the WFM GUI or via the workflow management REST API
The following parameters must be supplied

```
    "token_auth": The REST API Bearer token e.g."YWRtaW46Tm9raWFOc3AxIQ==",
    "rest_gateway_host": The IP address of the NSP REST gateway e.g.  "135.121.148.255",
    "ne1": The system address of the source node e.g. "11.11.11.11",
    "ne2": The system address of the destination node e.g. "33.33.33.33",
    "ne1port": The source port e.g. "1/1/12",
    "ne2port": The target port e.g. "1/1/12"
```

Additionally, the workflow may be initiated via the workflow management REST API

```
POST /wfm/api/v1/execution HTTP/1.1

{
    "workflow_id": "b0ceb995-b126-4798-b1e6-82db9bcfc9f7",
    "input": {
       "token_auth": "YWRtaW46Tm9raWFOc3AxIQ==",
       "rest_gateway_host": "135.121.148.255",
       "ne1": "11.11.11.11",
       "ne2": "33.33.33.33",
       "ne1port": "1/1/12",
       "ne2port": "1/1/12"
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

This project is licensed under the BSD-3 Clause License. See
[LICENSE.md](https://raw.githubusercontent.com/nokia/nsp-workflow/master/LICENSE.md) file for details
