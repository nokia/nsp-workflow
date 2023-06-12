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

---
# Port Audit

#### Restrictions
These workflow are using _Network Supervision_ to receive the list of available ports. Therefore NFMP managed and MDM managed devices including 3rd party devices are supported.

Keep in mind, that _Network Supervision_ requires an appropriate MDM adaptor to work. Also remind, that _Supervision Groups_ must be created accordance.

This workflow is for demoing purposes only.


#### Description
The workflow *portsInventory* retrieves the port inventory from which it renders a table as output.

The workflow *portsAudit* will execute successfuly, if all physical ports that are administratively enabled are operational up. If there are ports that are administratively enabled but operational down, the workflow execution will fail. If the audit fails a HTML table gets populated that contains all ports that violate the auditing criteria.