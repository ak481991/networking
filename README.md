# Cisco ISE Reference Pages

Two self-contained HTML study pages for network engineers working with Cisco Identity Services Engine. No build step, no dependencies beyond Google Fonts — open either file in a browser.

| File | Covers |
| --- | --- |
| `ise-reference.html` | ISE terminology across 17 domains: architecture and personas, AAA protocols and ports, 802.1X and access methods, EAP, the policy model, identity stores, PKI, profiling, posture, BYOD, guest, TrustSec, pxGrid, device administration, licensing, troubleshooting codes, plus 20 self-test questions |
| `eap-tls-ise.html` | EAP-TLS end to end at frame level: the three-party model, EAPOL/EAP/RADIUS header anatomy, a message-flow ladder diagram, the TLS 1.2 handshake message by message, fragmentation mechanics, key derivation, ISE-side certificate validation, authorisation and CoA, TLS 1.3 (RFC 9190) differences, failure signatures, and a lab demo runbook |

## Features

- Live keyword filter across every term and table row (press `/` to focus the search box)
- Light and dark themes, following the system preference with a manual override
- Per-section "Reviewed" checkboxes with progress saved in the browser
- Responsive down to phone width, and print-friendly

## Publishing as a site

Both files are static. To serve them with GitHub Pages: push to the default branch, then under **Settings → Pages** set the source to that branch and the root folder. The pages are reachable at `https://<user>.github.io/<repo>/ise-reference.html` and `.../eap-tls-ise.html`.

## Accuracy note

Port numbers, licence tier names, TLS version support and scale figures move between ISE releases. Confirm anything you intend to state as fact against the release notes, the Compatibility Guide, and the Performance and Scalability Guide for the exact version in question.

## Standards referenced

RFC 5216 (EAP-TLS), RFC 9190 (EAP-TLS 1.3), RFC 3748 (EAP), RFC 3579 (RADIUS support for EAP), RFC 2865/2866 (RADIUS), RFC 5176 (Change of Authorization), RFC 7170 (TEAP), IEEE 802.1X, IEEE 802.1AE.
