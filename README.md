# Networking Reference Pages

Self-contained HTML study pages for network engineers. No build step and no dependencies beyond Google Fonts — open any file in a browser.

Two files put every page behind one tab bar. Both keep the open tab in the URL hash, so a link can point at a specific page.

- **`index.html`** — the hub to use day to day, and the landing page when the repo is served with Pages. It loads each page from its own file, so edits to a page show up here with no further work, and it fetches a page only when its tab is first opened rather than all of them up front. Tabs respond to arrow keys, `Home` and `End`. Hashes are readable (`index.html#ospf`); a numeric hash from a bundle link still works and is rewritten to the slug.
- **`cisco-network-reference.html`** — one self-contained file with the nine reference pages embedded, for carrying offline or handing to someone as a single attachment. Because the pages are embedded, editing a reference page below does **not** change this file; regenerate it when the sources change.

Adding a page to the hub is one entry in the `PAGES` array at the top of the script in `index.html`.

## Interview preparation

Collapsed question-and-answer pages that work as a self-test: each answer opens to a short spoken response, the supporting detail, and a note on what the question is actually probing. Filter by keyword or by depth (Core / Deep / Expert), or reveal everything at once.

| File | Questions | Covers |
| --- | --- | --- |
| `interview-routing.html` | 67 | Forwarding fundamentals (RIB/FIB, CEF, recursion, uRPF), OSPF (LSA types, forwarding address, SPF triggers, ABR rules), EIGRP (feasibility condition, SIA, query scope, stub), BGP (best path, RR, MED comparability, aggregation, multipath, convergence, RPKI), redistribution and policy, MPLS/VRF, multicast, IPv6, HA and convergence budgets, overlays and segment routing, methodology, whiteboard scenarios |
| `interview-switching.html` | 61 | Frame forwarding and TCAM, VLANs and trunking (native VLAN, VTP, QinQ), spanning tree (path cost, RSTP mechanics, MST regions, TCN), STP protection (root vs loop guard, UDLD, storms), EtherChannel and MLAG, FHRP and anycast gateway, L3 switching and routed access, campus design and oversubscription, L2 security chain, data-centre switching (leaf-spine, VXLAN, incast, PFC/ECN), troubleshooting, whiteboard scenarios |
| `interview-security.html` | 61 | AAA and identity (RADIUS/TACACS+, EAP methods, MAB, ISE policy, CoA), firewall architecture (stateful tables, ASA order of operations, ASP drops, FTD, failover, asymmetry), NAT, ACLs and ZBFW, IPsec and IKEv2, VPN topologies (DMVPN, FlexVPN, GETVPN, remote access, SD-WAN), PKI and certificates, segmentation and TrustSec, infrastructure hardening (CoPP, TTL security, DDoS), monitoring and detection, incident response, whiteboard scenarios |

## Reference pages

| File | Covers |
| --- | --- |
| `packet-capture.html` | Packet capture across every platform family: where each tool taps the packet path, IOS-XE Embedded Packet Capture with filters and ACLs, Catalyst 9000 punt behaviour and limits, classic IOS and 6500/4500 tooling, SPAN/RSPAN/ERSPAN with the ERSPAN byte layout, punt/inject and FED counters, `debug platform condition`, QFP packet-trace with fia-trace, Catalyst 9800 and over-the-air capture, Nexus Ethanalyzer, SPAN-to-CPU and ELAM, NX-OS drop counters and CoPP, tcpdump/tshark and BPF, a "why the capture is empty" diagnostic, **ten worked incident scenarios**, and a 153-row searchable command reference |
| `wlc-reference.html` | Wireless LAN Controllers end to end: split-MAC architecture, CAPWAP, AP modes and the AP join process, switch configuration for local mode and FlexConnect, the 9800 tag model, client join flow for every security type, the 4-way handshake, roaming and mobility, RF fundamentals (RSSI, noise, SNR), channels and interference, RRM, security, troubleshooting tools, plus **ten worked incident scenarios** |
| `qos-reference.html` | QoS end to end: the ToS byte at bit level, DSCP/PHB and the RFC 4594 12-class model, classification, MQC, queuing and LLQ, WRED and ECN, policing and shaping with the token-bucket maths, hierarchical QoS, campus switch QoS and microbursts, WAN/MPLS tunnelling modes, wireless, design guidance, reading `show policy-map interface`, plus **ten worked incident scenarios** |
| `ospf-reference.html` | OSPF from fundamentals to operations against one multi-area lab topology: byte-level packet decode, the neighbor FSM, all network types, DR/BDR, every LSA type with flooding scope, area types, SPF and route selection, summarization, filtering, redistribution, virtual links, authentication, OSPFv3, scaling, troubleshooting, plus **ten worked incident scenarios** with real CLI output |
| `bgp-reference.html` | BGP from fundamentals to operations against one multihomed lab topology: path attributes, the 13-step best-path algorithm, iBGP and route reflectors, origination and aggregation, filtering and communities, multihoming and traffic engineering, scaling, MP-BGP, security and RPKI, troubleshooting, plus **ten worked incident scenarios** with real CLI output |
| `ise-reference.html` | Cisco ISE terminology across 17 domains: architecture and personas, AAA protocols and ports, 802.1X and access methods, EAP, the policy model, identity stores, PKI, profiling, posture, BYOD, guest, TrustSec, pxGrid, device administration, licensing, troubleshooting codes, plus 20 self-test questions |
| `eap-tls-ise.html` | EAP-TLS end to end at frame level: the three-party model, EAPOL/EAP/RADIUS header anatomy, a message-flow ladder diagram, the TLS 1.2 handshake message by message, fragmentation mechanics, key derivation, ISE-side certificate validation, authorisation and CoA, TLS 1.3 (RFC 9190) differences, failure signatures, and a lab demo runbook |
| `asa-reference.html` | Cisco ASA basics through advanced: platforms and architecture, the packet-flow order of operations as a diagram, interfaces and security levels, ACLs, NAT (all three sections), routing, MPF and inspection, connections and xlates, failover, clustering, site-to-site and remote-access VPN, multiple context mode, transparent mode, AAA, syslog IDs, ASP drop reasons, a troubleshooting workflow, and ASA vs FTD |
| `asa-nat.html` | Every ASA NAT type in depth against one lab topology: rule evaluation order, dynamic PAT, dynamic NAT, static NAT, static PAT, identity NAT and exemption, twice/policy NAT, hairpin and U-turn, DNS doctoring, NAT with VPN, PAT scaling, IPv6 NAT, troubleshooting, and a symptom-to-fix table. Includes packet transformation tables and three diagrams |

## Features

Every page shares the same behaviour:

- Live keyword filter across all terms and table rows — press `/` to focus the search box
- Light and dark themes, following the system preference with a manual override
- Per-section "Reviewed" checkboxes with progress saved in the browser
- Responsive down to phone width, and print-friendly
- Diagrams drawn as inline SVG, themed with the rest of the page

## Publishing as a site

All files are static. To serve them with GitHub Pages: push to the default branch, then under **Settings → Pages** set the source to that branch and the root folder. `index.html` is then served at `https://<user>.github.io/<repo>/` as the tabbed hub, and each page stays reachable on its own at `https://<user>.github.io/<repo>/<filename>`.

## Accuracy note

Command syntax, port numbers, licence tier names, defaults and scale figures all move between software releases. Confirm anything you intend to state as fact — or apply to production — against the configuration guide, command reference and release notes for the exact version in front of you.

## Standards referenced

RFC 5216 (EAP-TLS), RFC 9190 (EAP-TLS 1.3), RFC 3748 (EAP), RFC 3579 (RADIUS support for EAP), RFC 2865/2866 (RADIUS), RFC 5176 (Change of Authorization), RFC 7170 (TEAP), RFC 5737 (documentation address ranges), IEEE 802.1X, IEEE 802.1AE.
