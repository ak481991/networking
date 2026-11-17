# Networking Reference Pages

Self-contained HTML study pages for network engineers. No build step and no dependencies beyond Google Fonts — open any file in a browser.

| File | Covers |
| --- | --- |
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

All files are static. To serve them with GitHub Pages: push to the default branch, then under **Settings → Pages** set the source to that branch and the root folder. Each page is then reachable at `https://<user>.github.io/<repo>/<filename>`.

## Accuracy note

Command syntax, port numbers, licence tier names, defaults and scale figures all move between software releases. Confirm anything you intend to state as fact — or apply to production — against the configuration guide, command reference and release notes for the exact version in front of you.

## Standards referenced

RFC 5216 (EAP-TLS), RFC 9190 (EAP-TLS 1.3), RFC 3748 (EAP), RFC 3579 (RADIUS support for EAP), RFC 2865/2866 (RADIUS), RFC 5176 (Change of Authorization), RFC 7170 (TEAP), RFC 5737 (documentation address ranges), IEEE 802.1X, IEEE 802.1AE.
