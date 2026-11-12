# Awesome Network Protocol Visualizers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated, honest list of tools that help you **see** network protocols — from full packet capture to byte-level parsers to interactive learning apps.

> This list is maintained honestly. Every entry states what the tool *is*, what it is *best for*, and what it is *not*. No tool here is "the best" for everyone; they occupy different points on the spectrum between *capturing real traffic* and *learning a concept*.

*Companion essay (10 languages): [Seeing the Invisible — Multilingual](articles/README.md).*

## Contents

- [Why this list exists](#why-this-list-exists)
- [Packet analyzers (capture & dissect)](#packet-analyzers-capture--dissect)
- [Byte-level parsers & visualizers](#byte-level-parsers--visualizers)
- [Interactive learning apps](#interactive-learning-apps)
- [Structured courses & lessons](#structured-courses--lessons)
- [How to choose](#how-to-choose)
- [Contributing](#contributing)
- [License](#license)

## Why this list exists

"Network protocol visualizer" is a vague phrase. One person means *Wireshark capturing packets on a live interface*; another means *a web page that turns a hex string into colored protocol fields*; a third means *an animated TCP handshake*. All three are legitimate, and all three are different tools.

This list groups them by what they actually do, so you can pick the right one instead of the most famous one.

## Packet analyzers (capture & dissect)

### [Wireshark](https://www.wireshark.org/)

- **What it is:** The open-source, industry-standard packet analyzer. Captures live traffic from a network interface and dissects thousands of protocols down to the field level.
- **Best for:** Real-world debugging, protocol development, security analysis, and anything that requires looking at *actual* traffic on a wire.
- **Not for:** Quickly understanding a single protocol's structure in isolation, or learning concepts without a capture setup. It is powerful and correspondingly heavy; newcomers are often overwhelmed by the raw volume of a live capture.
- **License:** Open source (GPLv2). Desktop: Windows, macOS, Linux.

## Byte-level parsers & visualizers

### [ByteLens](https://bytelens.dev/)

- **What it is:** A free, browser-based protocol visualizer and packet parser. Paste raw hex (or load an example or PCAP) and see each protocol layer, header field, byte range, and decoded value in one interactive view. Parsing happens entirely in your browser — nothing is uploaded to a server.
- **Best for:** Understanding how protocol headers are laid out at the byte level, debugging a known packet, teaching, and documenting examples. Also ships a PCAP viewer and a MAC OUI lookup.
- **Not for:** Capturing live traffic. It analyzes bytes you already have; it is not a sniffer.
- **Protocols:** Ethernet II, IPv4, IPv6, TCP, UDP, DNS, Kafka, Redis RESP. Free, no registration.

## Interactive learning apps

### [Protocols Visualizer](https://protocols-visualizer.vercel.app/en)

- **What it is:** A free, interactive web app for *learning* network protocols. Built around the OSI model's seven layers, each protocol offers Communication Flow (animated sequence diagrams), Packet Anatomy (interactive headers), and Attack Simulation (e.g. SYN Flood, ARP Spoofing, deauth, Bad USB). Available in English and Portuguese.
- **Best for:** Students, teachers, and the curious who want to *see* handshakes, routing, and attacks in motion rather than read about them.
- **Not for:** Analyzing real captures or dissecting arbitrary packets. It is a teaching simulation, not an analyzer.
- **Stack:** Next.js, React, TypeScript, Tailwind CSS.

## Structured courses & lessons

> **Disclosure:** *Protocol Explorer is maintained by the author of this list.* It is included because it fits the category honestly, not because it paid to be here.

### [Protocol Explorer](https://protocolexplorer.run/)

- **What it is:** A guided, curriculum-style learning product for network protocols. Structured, step-by-step lessons span 33 protocols (HTTP, HTTPS, and more), each broken into annotated steps.
- **Best for:** Learners who want a path to follow rather than a reference to browse — a course, not a tool. The free tier covers HTTP and HTTPS with the first three steps of every lesson; a one-time $4.99 Pro unlocks all 33 protocols and every step.
- **Not for:** Live capture or byte-level parsing. It teaches; it does not dissect traffic.
- **Model:** Free + one-time Pro. Sign-in via Clerk, payments via Stripe.

## How to choose

| If you need to… | Start with |
|---|---|
| Capture and dissect *real* traffic on a live network | **Wireshark** |
| Turn a known hex string or PCAP into readable protocol fields, privately in-browser | **ByteLens** |
| *See* handshakes, routing, and attacks animated for learning | **Protocols Visualizer** |
| Follow a structured, step-by-step course across many protocols | **Protocol Explorer** |

None of these replace the others. The right one depends on whether you are *capturing*, *parsing*, *visualizing a concept*, or *following a curriculum*.

## Contributing

Know a tool that belongs here and is honest about what it does? Open a pull request. Keep entries factual: what it is, what it's best for, what it is not. Promotional copy that hides limitations will be edited or declined.

## License

[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) — this list is public domain. The tools listed retain their own respective licenses.
