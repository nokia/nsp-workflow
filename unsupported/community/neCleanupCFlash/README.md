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
# Cleanup CF

#### Restrictions
These workflows are for demoing purposes only.

#### Description
The use-case is about removing files from the NE filesystem based on age as house keeping operation. The use is limited to Nokia SR OS device in MD-MODE (managed via MDM).

To understand best-practice workflow programming principles including performance impact, multiple versions of this workflow are provided.

**Version 1**

Initial version of this workflow, to understand the basic principles of such workflow. While `concurrency` is supported, it will result in multiple concurrent CLI sessions to the same device. For every execution of `nsp.mdm_cli` a new SSH session is established.

**Version 2**

MDM's CLI framework supports session re-use. That means, that the same CLI session is re-used for multiple `nsp.mdm_cli` executions. This provides performance benefits against version 1, as the SSH session does not need to be established, authenticated and closed for every file to be delete.

**Version 3**

Instead of iterating over the list of files to remove, in version 3 JavaScript is used to compile a list of CLI commands to perform the actual removal. This list will be used as payload of a single `nsp.mdm_cli` action execution. Overhead in WFM engine/executor and number of DB transaction gets reduced.

**Version 4**

Same as version 3, but simplief. Avoid the use of JavaScript to compile the MD-CLI payload. Instead YAQL is used, so workflow gets much more cleaned up.