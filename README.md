# Hi, ich bin Smilez1985 🛠

**Systems & Platform Architect | Local-First AI Infrastructure | DevSecOps & Integration**

Ich bin Fachinformatiker für Systemintegration (FiSi) aus dem Saarland und baue air-gapped Infrastrukturen sowie autonome KI-Systeme für Edge-Hardware und Developer Tools, die LLMs, Vision-Engines und RAG-Systeme stabil, asynchron und sicher auf echte Edge-Hardware (ARM, Rockchip-NPUs, Handhelds) bringen.

In meinem Homelab betreibe ich ein heterogenes Mesh-Netzwerk aus autonomen KI-Agenten auf Samsung-Smartphones und Linux-Knoten mit einem modifizierten Agentic Harness auf Basis von **[OpenMinis](https://github.com/OpenMinis/OpenMinis)**. Mein Ziel-Fokus liegt auf digitaler Souveränität: **KI unabhängig von Big-Tech-Serverfarmen, lokal optimiert, asynchron gekoppelt und kryptografisch gehärtet.** Parallel entwickle ich mit **[Chimera](https://github.com/Smilez1985/chimera)** ein eigenes Linux-basiertes Agentic Harness mit direkter **wake on agent - loop**-Integration.

Ich nutze Frontier-LLMs als „Code-Monkey“ für die Syntax, während meine eigentliche Stärke in der Systemarchitektur, rootless Container-Isolierung, asynchronen Kommunikationsschleifen und logischen Absicherung nach Enterprise-Vorgaben liegt.

---

## 🚀 Mein Core-Ökosystem (Einsatzbereit für Edge, Robotik & Air-Gap)

### 1. 🔌 [PiPortal](https://github.com/Smilez1985/PiPortal)) *(v1.4.0 · Hardware-verifiziert)*
*Mobile Air-Gap-Bridge und abgeschottete Admin-Workstation im USB-Stick-Format.*
Verwandelt einen Raspberry Pi Zero 2 W per `configfs/libcomposite` in ein treiberloses USB-Composite-Gadget (NCM/RNDIS + FAT16-Wegweiser) mit eigenem WLAN-Uplink, gehärtetem SMB, optionalem Tailscale/Headscale und integrierter Claude Code CLI (`piportal start claude`) auf 512 MB RAM (`zram`). Abgeschlossen und an Windows-11-Hardware verifiziert.

### 2. 🏗 [LLM_Cross-Compiler_Framework (LLMCF)](https://github.com/Smilez1985/LLM_Cross-Compiler_Framework)) *(v3.4.0)*
*Zähmt das Chaos proprietärer Hardware-SDKs – von der Quantisierung bis zum signierten Board-Bündel.*
Kapselt Compiler-Toolchains (Rockchip RKNN/RKLLM, `llama.cpp`, `whisper.cpp`) in isolierten rootless Container-Sandboxes mit Offline-Preload-Pipelines. Automatisiert den Weg von Hugging-Face-Gewichten über GGUF und RKLLM/RKNN inklusive Auto-Tuning (IMatrix) bis zum deterministischen Deployment via `systemd`-Units auf Ziel-SBCs, ergänzt durch eigene Rust-Daemons (`#![forbid(unsafe_code)]`). Auf Stand `v3.4.0` (`development`-Branch).

### 3. 🤖 [Chimera](https://github.com/Smilez1985/chimera) *(Pre-Alpha · läuft auf Hardware)*
*Ein gehärtetes Agentic Harness mit eigenem Gesicht und offline-fähiger Stimme.*
Vernetzt einen Raspberry Pi Zero 2 W (mit PiSugar Whisplay HAT) als eigenständigen Linux-Agenten mit dynamischem Gesicht, RGB-LED und lokaler Spracherkennung/-synthese via `sherpa-onnx`. Bietet dualen Voice/Telegram-Zugang, ein winziges Rust-Gateway (`chimera-tor`, 1,6 MB RAM) sowie das selbstheilende Subsystem **Mojo** mit Reboot-Überleben.

### 4. 🧠 [rag4ll](https://github.com/Smilez1985/rag4ll) *(in Entwicklung / noch privat)*
*Markdown-first, framework-agnostische RAG-Memory für dezentrale Agenten.*
Bietet langlebiges, block-bewusstes Markdown-Gedächtnis mit erhaltenen Heading-Paths und Code-Grenzen über die Laufzeit einzelner Agenten hinaus. Nutzt Qdrant Edge, Tor-Isolation und einen PSK-gesicherten Inter-Agent-Message-Bus mit TTL-Nachrichtenbestätigung sowie ein Lazy-Load-Embedding- und Rerank-Sidecar zur automatischen GPU-Freigabe im Leerlauf.

### 5. 🔔 [woa-l – Wake on Agent Loop](https://github.com/Smilez1985/woa-l) *(in Entwicklung / noch privat)*
*Asynchrones, batteriesparendes Event-Routing für autonome Schleifen.*
Löst das Problem nicht-persistenter Zwischen-Nachrichten-Prozesse durch ein ereignisgesteuertes Aufweck-Protokoll: Eine HTTP-Klingel in der Agenten-Sandbox lauscht auf JSON-RPC-Signale (MCP über HTTP) mit At-least-once-Zustellung, injiziert den Reiz als Prompt, reaktiviert den Agenten für einen Turn und schläft ihn sofort wieder ein.

### 6. **[Noisy | The Mood-Mochi](https://github.com/Smilez1985/Noisy) :** Passiver "Ambient Lifeform" auf einem Pi Zero 2 WH. (Quasi mein "Hello World")

---

## 🛡 Mein Security- & FiSi-Mindset

Durch permanentes Dogfooding härte ich autonome Agenten gegen Systemrisiken ab:
- **Strikte Sandbox-Kapselung:** Rootless Podman/Docker, schreibgeschützte Laufzeit-Layer und gepinnte Image-Digests.
- **Eigene Rust-Sicherheitsgrenzen:** Privilegierte Board-Operationen, SPAKE2-SSH-Kopplung und Gateways über statisch gelinkte Rust-Binaries (`#![forbid(unsafe_code)]`).
- **Supply-Chain- & Code-Prüfung:** Trivy-Vulnerability-Scans, CodeQL, Secret-Scans und HMAC-verkettete Audit-Logs in der Pipeline.
- **Prompt-Injection-Abwehr:** Konsequentes Input-Sanitizing, Capability-Gating und Human-in-the-Loop-Freigaben für destruktive Aktionen.

---

## 🎯 Was ich suche:

Ich suche Rollen im Bereich **Sovereign & Embedded AI** (remote oder Saarland).

**Kontakt:** Schreibt mir direkt hier über GitHub oder stoßt eine Diskussion in den Repositories an. *Let's talk Tech.*
