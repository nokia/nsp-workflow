
# Nokia NSP 
## NRCP - Site Health Monitoring

### Description
Automatical switchover to standby cluster can be triggered by CprotoChannelDown alarm

### Version
NRCP - site health monitoring - version 1.0

### Support level
Support signed version

### History
|Version|Author|Date      |Comments     |
|:-------|:------|:----------|:-------------|
|   1.0 |  SW  |2019-11-13|NSP19.11 updates|

### Prerequisites
Nokia NSP with Workflow Manager and NRCP

### Tested with
* Nokia NSP 19.11

### Installation
Workflow can directly be imported/updated from nsp-workflows using the WFM WebUI.

### Usage
The primary site VSR-NRC may lose cproto channel connectivity to the NRC-P. It is desirable in this case to provide a automatic site switchover functionality.
The site health monitoring function can be configured optionally on NSP.

NRC-P raises a CprotoChannelDown alarm when the first Cproto channel goes down. The workflow will be triggered by this alarm. After a configurable
down timer (default delay is 5 minutes) expires, the workflow checks whether the cprotoChannelDown alarm has been cleared or not. If cleared, it means cproto
connectivity is up, and the workflow doesn't continue. If the alarm still exists, the workflow will ping the VSR-NRC at the inactive DR site to check
whether it is in better shape before initiating site switchover.

The following needs to be configured in order to use site health monitoring function:

1) Create a new kafka Trigger on WFM WebUI

Workflow name: switchover

Trigger rule: $[?(@.alarmName == 'CprotoChannelDown' && @.severity == 'major')]

Kafka topic: nsp-db-fm

Kafka Event: create

Enabled: True

2) Add the following items in Environment file DefaultEnv using the WFM WebUI

```yaml
username: "root";
password: "NokNsp1!"
ping_duration: 3
delay: 300
site1_vsr: xxx.xxx.xxx.xxx
site1_wfm: xxx.xxx.xxx.xxx
site1_vip_advertised: xxx.xxx.xxx.xxx
site2_vsr: xxx.xxx.xxx.xxx
site2_wfm: xxx.xxx.xxx.xxx
site2_vip_advertised: xxx.xxx.xxx.xxx
site2_sdn1: xxx.xxx.xxx.xxx
site2_sdn2: xxx.xxx.xxx.xxx
site2_sdn3: xxx.xxx.xxx.xxx
```

**Notes:**
a) On 1+1 HA setup, put "null" as the values of site2_sdn2 and site2_sdn3.
b) If Openstack setup is used, site2_sdn1, site2_sdn2, site2_sdn3, site1_wfm, and site2_wfm are private IP addresses.

