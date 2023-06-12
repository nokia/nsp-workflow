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
# Nokia SR OS パケットキャプチャ

#### 制限事項
本ワークフローはデモ用途です。
 
#### 説明
ノード番号とポート番号、サンプル時間の指定が必要です。
pcapファイルをノード上のCF3に作成し、サンプル時間を経過しますと、CF上のファイルに保存します。
その後pcapファイルをダウンロードします。取得したpcapファイルはwiresharkで閲覧したり、tcpdumpにてデコード可能となります。

---
# Packet Capture for Nokia SR OS

#### Restrictions
This workflow is for demoing purposes only.

#### Description
Provide NE Id, Port and sample duration. A pcap-file will be created on the nodal CF3: card and downloaded after the sample duration has been passed. The pcap-file will be downloaded by WFM for later usage. In addition, the workflow will leverage the LINUX tool `tcpdump` to decode the pcap-file.