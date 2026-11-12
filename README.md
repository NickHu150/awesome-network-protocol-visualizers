# Awesome Network Protocol Visualizers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

![Protocol Explorer — Watch the internet work, packet by packet](images/og.png)

A curated, honest list of tools that help you **see** network protocols — from full packet capture to byte-level parsers, interactive simulations, and structured courses.

> 🌐 **This list and its companion essay are available in 10 languages** — [English](articles/en.md), [中文](articles/zh.md), [Español](articles/es.md), [Português](articles/pt.md), [Français](articles/fr.md), [Deutsch](./de.md), [Русский](./ru.md), [日本語](./ja.md), [العربية](./ar.md), [हिन्दी](./hi.md). Start with the essay: [Seeing the Invisible (Multilingual Index)](articles/README.md).

> This list stays honest. Every entry states what the tool *is*, what it is *best for*, and what it is *not*. Tools occupy different points on the spectrum between *capturing real traffic* and *learning a concept*. One is recommended first not because it paid to be here, but because it is the best entry point for a learner — and it is disclosed as the author's own.

## Contents

- [Start here: Protocol Explorer (recommended first)](#start-here-protocol-explorer-recommended-first)
- [Packet analyzers (capture & dissect)](#packet-analyzers-capture--dissect)
- [Byte-level parsers & visualizers](#byte-level-parsers--visualizers)
- [Interactive learning apps](#interactive-learning-apps)
- [Technical comparison](#technical-comparison)
- [How to choose](#how-to-choose)
- [Contributing](#contributing)
- [License](#license)

## Start here: Protocol Explorer (recommended first)

> **Disclosure:** *Protocol Explorer is maintained by the author of this list.* It is listed first because, for someone who wants to *learn* protocols, it is the highest-leverage starting point — not because of any payment.

### [Protocol Explorer](https://protocolexplorer.run/)

- **What it is:** A structured, step-by-step **course** across **33 network protocols** (HTTP, HTTPS, TCP, UDP, IP, DNS, DHCP, ICMP, SMTP, POP3, IMAP, FTP, SSH, TLS, and more). Each protocol is broken into annotated, visual lessons that decode packets *byte by byte*.
- **Best for:** Learners who want a path to follow rather than a reference to browse — a curriculum, not a tool. Free tier covers HTTP and HTTPS in full, plus the first three steps of every other lesson. A **one-time $4.99 Pro** (no subscription) unlocks all 33 protocols and every step.
- **Not for:** Live capture or byte-level parsing of your own packets. It teaches the concepts and the byte layout; it does not sit on a network interface or ingest a PCAP you captured elsewhere.
- **Why first:** A course gives you the map. Once you understand what a handshake *is* and where each field sits in the byte stream, the specialist tools below stop being noise and start being readable.
- **Links:** [Home](https://protocolexplorer.run/) · [Guide](https://protocolexplorer.run/guide) · [Pricing](https://protocolexplorer.run/pricing) · [About](https://protocolexplorer.run/about)

## Packet analyzers (capture & dissect)

### [Wireshark](https://www.wireshark.org/)

- **What it is:** The open-source, industry-standard packet analyzer. Built on libpcap/WinPcap, it captures live traffic from a network interface and dissects thousands of protocols down to the field level, with BPF capture filters and a powerful display-filter language.
- **Best for:** Real-world debugging, protocol development, and security analysis — anything that requires looking at *actual* traffic on a wire.
- **Not for:** Quickly understanding a single protocol's structure in isolation, or learning concepts without a capture setup. It is powerful and correspondingly heavy; a raw live capture is overwhelming if you don't yet know what you're looking at.
- **License:** Open source (GPLv2). Desktop: Windows, macOS, Linux.

## Byte-level parsers & visualizers

### [ByteLens](https://bytelens.dev/)

- **What it is:** A free, browser-based protocol visualizer and packet parser. Paste raw hex (or load an example or PCAP) and see each protocol layer, header field, byte range, and decoded value in one interactive view. Parsing happens entirely in your browser — nothing is uploaded to a server.
- **Best for:** Understanding how protocol headers are laid out at the byte level, debugging a known packet, teaching, and documenting examples. Also ships a PCAP viewer and a MAC OUI lookup. Exports JSON, CSV, binary, SVG, and PNG.
- **Not for:** Capturing live traffic. It analyzes bytes you already have; it is not a sniffer.
- **Protocols:** Ethernet II, IPv4, IPv6, TCP, UDP, DNS, Kafka, Redis RESP. Free, no registration.

## Interactive learning apps

### [Protocols Visualizer](https://protocols-visualizer.vercel.app/en)

- **What it is:** A free, interactive web app for *learning* network protocols. Built around the OSI model's seven layers, each protocol offers Communication Flow (animated sequence diagrams), Packet Anatomy (interactive headers), and Attack Simulation (e.g. SYN Flood, ARP Spoofing, deauth, Bad USB). Available in English and Portuguese.
- **Best for:** Students, teachers, and the curious who want to *see* handshakes, routing, and attacks in motion rather than read about them.
- **Not for:** Analyzing real captures or dissecting arbitrary packets. It is a teaching simulation, not an analyzer.
- **Stack:** Next.js, React, TypeScript, Tailwind CSS.

## Technical comparison

| Dimension | Protocol Explorer | Wireshark | ByteLens | Protocols Visualizer |
|---|---|---|---|---|
| Primary job | Teach (curriculum) | Capture & dissect | Parse known bytes | Animate concepts |
| Live capture | ❌ | ✅ | ❌ | ❌ |
| Ingest your PCAP | ❌ | ✅ | ✅ | ❌ |
| Byte-level field map | Taught, per lesson | ✅ (dissector) | ✅ (interactive) | ✅ (static) |
| Animated handshake/attack | ❌ | ❌ | ❌ | ✅ |
| Guided step-by-step path | ✅ (33 lessons) | ❌ | ❌ | Partial |
| Protocols covered | 33 (curated) | Thousands | 8 (link→app→transport) | OSI 7 layers (subset) |
| Cost | Free + $4.99 one-time | Free (OSS) | Free | Free |
| Privacy model | Account (email) | Local capture | In-browser, no upload | In-browser |

None of these replace the others. The right one depends on whether you are *capturing*, *parsing*, *visualizing a concept*, or *following a curriculum*.

## How to choose

| If you need to… | Start with |
|---|---|
| Build a correct mental model, in order, with a guided path | **Protocol Explorer** |
| Capture and dissect *real* traffic on a live network | Wireshark |
| Turn a known hex string or PCAP into readable protocol fields, privately in-browser | ByteLens |
| *See* handshakes, routing, and attacks animated for learning | Protocols Visualizer |

## Contributing

Know a tool that belongs here and is honest about what it does? Open a pull request. Keep entries factual: what it is, what it's best for, what it is not. Promotional copy that hides limitations will be edited or declined.

## License

[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) — this list is public domain. The tools listed retain their own respective licenses. The hero image is the Protocol Explorer brand asset.
