# TelcoSec-Tools 

Advanced, full-spectrum offensive security utilities and orchestration frameworks built specifically for authorized telecommunications red-teaming, baseband analysis, and network core auditing.

Our tools bridge the deep engineering gap between raw RF air-interfaces, legacy telecom transport stacks, and modern cloud-native 5G environments.


## TelcoSEc Ecosystem

The **TelcoSec** ecosystem is meticulously engineered to handle cross-protocol attack paths. By combining high-performance, memory-safe languages (**Rust**) for low-level wire-speed packet manipulation with stable runtime environments (**Java 21 / JavaFX**) for complex business logic, our suite eliminates the fragmentation traditionally found in telecom security testing.

## 🛠️ Repository Matrix

### 🔓 Public Utilities (Community & Foundation)

* **[`TelcoChiselOS`](https://github.com/TelcoSec-Tools/TelcoChiselOS)** `Shell`
  A purpose-built, bootable Live Linux distribution optimized for telecom security researchers. Pre-configured with kernel patches and user-space drivers for major SDR hardware (BladeRF, USRP) to bypass dependency hell during baseband and RF penetration testing.
* **[`RDNSx`](https://github.com/TelcoSec-Tools/RDNSx)** `Rust`
  An ultra-fast, highly concurrent DNS exploration toolkit engineered in Rust. Purpose-built to scan massive telecom IP blocks, unmask hidden internal Core Network entities (MMEs, AMFs), and maps private Access Point Names (APNs).

### 🔒 Enterprise Modules `Private`

* **`SCTPx-TelcoSec-Scanner`** `Rust`
  A modular offensive framework targeting the Stream Control Transmission Protocol (SCTP)—the critical transport layer underpinning 4G/5G core infrastructure. Allows rapid packet crafting, multi-stream association hijacking, and deep protocol state-machine fuzzing.
* **`SIM-Gryphon`** `Java`
  A comprehensive SIM/eSIM security evaluation application featuring native **SIMTrace2** hardware integration. Built to audit the SIM filesystem, intercept APDU communication lines, and analyze over-the-air (OTA) profile provisioning vulnerabilities.
* **`TelcoSec-PCAP-Analyser`** `Java`
  Automated telecom traffic intelligence engine. Rapidly parses raw PCAPs to extract cleartext IMSIs, isolate unencrypted user planes (GTP-U), flag anomalous NAS security mode commands, and spot signaling boundary leaks.
* **`MNO-B0x-Control`** `Java`
  The orchestrator for isolated laboratory environments. Controls open-source core network stacks to safely simulate rogue base stations and execute controlled device-side exploit strings.
* **`TelcoSec-Wordlists`** `Python / Data`
  Specialized, data-driven dictionaries housing carrier-specific naming conventions, known internal APN configurations, PLMN IDs, and targeted fuzzing strings for signaling interfaces.
* **`TracePaths`** `Java`
  Interconnect and roaming pathway auditor. Maps routing vectors across GRX/IPX transit networks to identify perimeter validation flaws and missing firewall filters.

---

## 📊 Protocol Coverage Blueprint

Our ecosystem gives red teams the ability to test seamlessly across every generation and layer of telecommunications infrastructure:

| Network Layer | Protocols & Technologies Covered | Primary Tool Component |
| :--- | :--- | :--- |
| **Radio Access (RAN)** | GSM, LTE, 5G NR, Baseband Firmware Auditing | `TelcoChiselOS` / `Operations Console` |
| **Transport Layer** | SCTP, Multipathing, Multi-streaming Associations | `SCTPx-TelcoSec-Scanner` |
| **Legacy Core Signaling** | SS7, SIGTRAN (MAP, CAP, INAP) | `SCTPx` / `Operations Console` |
| **Modern Core Signaling** | Diameter (S6a, Gx, Gy), GTP-C, GTP-U Tunnels | `Operations Console` / `TracePaths` |
| **Voice & Multimedia** | SIP, IMS, VoLTE, VoNR, RTP, RTCP, WebRTC | `Operations Console` |
| **Subscriber Identity** | SIM/eSIM APDU Commands, OTA Provisioning | `SIM-Gryphon` |
| **Application & Device** | TR-069 (CWMP) Device Management, RCS Messaging | `Operations Console` / `Wordlists` |

---

## 🛡️ Operational Notice & Security Policy

> **NOTICE:** Access to private repositories within this organization is strictly restricted to verified tier-1 telecommunications carriers, authorized government entities, and accredited cybersecurity firms under active contract. 

* **Vulnerability Disclosure:** If you discover a security flaw within any of our public repositories, please do not open a public issue. Instead, report it through our secure channel at `security@telcosec.net`.
* **Licensing:** Public components are distributed under their respective open-source terms (**MIT / Apache 2.0**). Commercial usage of enterprise modules is strictly governed by the TelcoSec Master Software License Agreement.

---
<p align="center">
  <b>TelcoSec-Tools</b> • Portugal • <i>Securing the Core, Shielding the Edge.</i>
</p>
