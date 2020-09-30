<svg xmlns="http://www.w3.org/2000/svg" fill=#244c95 height=18>
  <symbol id="nokia" overflow="visible">
    <path d="M66 44 31 1H0V59H18V15L54 59H84V1H66V44" />
    <path d="M151 38C151 42 151 43 150 44 149 44 148 45 144 45H115C111 45 110 44 109 44 108 43 107 42 107 38V21C107 17 108 16 109 15 110 15 111 14 115 14H144C148 14 149 15 150 15 151 16 151 17 151 21ZM144 0H114C104 0 98 1 95 5 92 8 91 10 91 18V41C91 49 92 52 95 54 98 58 104 59 114 59H144C155 59 160 58 164 54 166 52 168 49 168 41V18C168 10 166 8 164 5 160 1 155 0 144 0Z" />
    <path d="M249 1H225L194 28 227 59H253L216 28ZM175 1V59H194V1Z" />
    <path d="M257 59H275V1H257Z" />
    <path d="M311 36 322 15 333 36ZM334 1H311L278 59H299L304 49H340L345 59H367Z" />
  </symbol>
  <use xlink:href="#nokia" transform="scale(0.3)" />
</svg>

# Workflows to manage BTS transport ran applications to transport IP service


## Objectives
For BTS MDM managed nodes:
- List the RAN Applications
- Bind a RAN Application to a transport service
- Unbind a RAN Application



#### Prerequisites

- SFERIC backend has been installed
- TBTS nodes discovered using MDM and physical links between the BTS and its neighbours 
- Upload the provided workflows and actions to the WFM server



#### Input parameters
bindRanApplication

```yaml
    - mrbts : This is the MRBTSID to be selected from all the discovered MRBTS (TBTS)
    - ranapplication : The ran application to bind to be selected amongst all the RAN Application of the selected mrbts
    - transportservice : The transort service name to bind to, to be selected amongst all the transport services created on the first router the BTS is connected to
    - ipAddressv4 : The IPV4 address to be configured in the BTS transport for IPV4 ran application, should be in the same subnet as the transport service
    - ipAddressv6 : The IPV6 address to be configured in the BTS transport for IPV6 ran application, should be in the same subnet as the transport service
    - vlan: The VLANID to be configured in the BTS transport, must be the same VLANID as the one configured on the transport service.
```

unbindRanApplication 

```yaml
    - mrbts : This is the MRBTSID to be selected from all the discovered MRBTS (TBTS)
    - ranapplication : The ran application to bind to be selected amongst all the RAN Application of the selected mrbts
```
