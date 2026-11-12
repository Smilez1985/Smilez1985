# Hi, ich bin Smilez1985 🛠

**Systems & Platform Architect | Local-First AI Infrastructure | DevSecOps & Integration**

Ich bin Fachinformatiker für Systemintegration (FiSi) aus dem Saarland und baue die schockresistente, air-gapped Infrastruktur, die LLMs, Vision-Engines und RAG-Systeme stabil, asynchron und sicher auf echte Edge-Hardware (ARM, Rockchip-NPUs, Handhelds) bringt.

In meinem Homelab betreibe ich ein heterogenes Mesh-Netzwerk aus autonomen KI-Agenten auf Samsung-Smartphones und Linux-Knoten mit einem modifizierten Agentic Harness auf Basis von **[OpenMinis](https://github.com/OpenMinis/OpenMinis)**. Mein Fokus liegt auf digitaler Souveränität: **KI unabhängig von Big-Tech-Serverfarmen, lokal optimiert, asynchron gekoppelt und kryptografisch gehärtet.** Parallel entwickle ich mit **[Chimera](https://github.com/Smilez1985/chimera)** ein eigenes Linux-basiertes Agentic Harness mit direkter **woa-l**-Integration.

Ich nutze LLMs hocheffizient als Syntax-Zuarbeiter, während meine eigentliche Stärke in der Systemarchitektur, rootless Container-Isolierung, asynchronen Kommunikationsschleifen und logischen Absicherung nach Enterprise-Vorgaben liegt.

---

## 🚀 Mein Core-Ökosystem (Einsatzbereit für Edge, Robotik & Air-Gap)

### 1. 🔌 [PiPortal](https://github.com) *(v1.4.0 · Hardware-verifiziert)*
*Mobile Air-Gap-Bridge und abgeschottete Admin-Workstation im USB-Stick-Format.*
Verwandelt einen Raspberry Pi Zero 2 W per `configfs/libcomposite` in ein treiberloses USB-Composite-Gadget (NCM/RNDIS + FAT16-Wegweiser) mit eigenem WLAN-Uplink, gehärtetem SMB, optionalem Tailscale/Headscale und integrierter Claude Code CLI (`piportal start claude`) auf 512 MB RAM (`zram`). Abgeschlossen und an Windows-11-Hardware verifiziert.

### 2. 🏗 [LLM_Cross-Compiler_Framework (LLMCF)](https://github.com) *(v3.4.0)*
*Zähmt das Chaos proprietärer Hardware-SDKs – von der Quantisierung bis zum signierten Board-Bündel.*
Kapselt Compiler-Toolchains (Rockchip RKNN/RKLLM, `llama.cpp`, `whisper.cpp`) in isolierten rootless Container-Sandboxes mit Offline-Preload-Pipelines. Automatisiert den Weg von Hugging-Face-Gewichten über GGUF und RKLLM/RKNN inklusive Auto-Tuning (IMatrix) bis zum deterministischen Deployment via `systemd`-Units auf Ziel-SBCs, ergänzt durch eigene Rust-Daemons (`#![forbid(unsafe_code)]`). Auf Stand `v3.4.0` (`development`-Branch).

### 3. 🤖 [Chimera](https://github.com/Smilez1985/Chimera) *(Pre-Alpha · läuft auf Hardware)*
*Ein gehärtetes Agentic Harness mit eigenem Gesicht und offline-fähiger Stimme.*
Vernetzt einen Raspberry Pi Zero 2 W (mit PiSugar Whisplay HAT) als eigenständigen Linux-Agenten mit dynamischem Gesicht, RGB-LED und lokaler Spracherkennung/-synthese via `sherpa-onnx`. Bietet dualen Voice/Telegram-Zugang, ein winziges Rust-Gateway (`chimera-tor`, 1,6 MB RAM) sowie das selbstheilende Subsystem **Mojo** mit Reboot-Überleben.

### 4. 🧠 rag4ll *(in Entwicklung / noch privat)*
*Markdown-first, framework-agnostische RAG-Memory für dezentrale Agenten.*
Bietet langlebiges, block-bewusstes Markdown-Gedächtnis mit erhaltenen Heading-Paths und Code-Grenzen über die Laufzeit einzelner Agenten hinaus. Nutzt Qdrant Edge, Tor-Isolation und einen PSK-gesicherten Inter-Agent-Message-Bus mit TTL-Nachrichtenbestätigung sowie ein Lazy-Load-Embedding- und Rerank-Sidecar zur automatischen GPU-Freigabe im Leerlauf.

### 5. 🔔 woa-l – Wake on Agent Loop *(in Entwicklung / noch privat)*
*Asynchrones, batteriesparendes Event-Routing für autonome Schleifen.*
Löst das Problem nicht-persistenter Zwischen-Nachrichten-Prozesse durch ein ereignisgesteuertes Aufweck-Protokoll: Eine HTTP-Klingel in der Agenten-Sandbox lauscht auf JSON-RPC-Signale (MCP über HTTP) mit At-least-once-Zustellung, injiziert den Reiz als Prompt, reaktiviert den Agenten für einen Turn und schläft ihn sofort wieder ein.

*(Einstiegsprojekt: **[Noisy](https://github.com)** – ein passiver emotionaler Audio-Begleiter mit Echtzeit-Sound-Erkennung und Konami-Code-Passwort-Reset auf dem Pi Zero 2 WH).*

---

## 🛡 Mein Security- & FiSi-Mindset

Durch permanentes Dogfooding härte ich autonome Agenten gegen Systemrisiken ab:
- **Strikte Sandbox-Kapselung:** Rootless Podman/Docker, schreibgeschützte Laufzeit-Layer und gepinnte Image-Digests.
- **Eigene Rust-Sicherheitsgrenzen:** Privilegierte Board-Operationen, SPAKE2-SSH-Kopplung und Gateways über statisch gelinkte Rust-Binaries (`#![forbid(unsafe_code)]`).
- **Supply-Chain- & Code-Prüfung:** Trivy-Vulnerability-Scans, CodeQL, Secret-Scans und HMAC-verkettete Audit-Logs in der Pipeline.
- **Prompt-Injection-Abwehr:** Konsequentes Input-Sanitizing, Capability-Gating und Human-in-the-Loop-Freigaben für destruktive Aktionen.

---

## 🛠 Tech-Stack in der Praxis

- **Infrastruktur & OS:** Linux (Debian, DietPi, Alpine), `systemd`, `cgroups`, `configfs`-USB-Gadgets, Udev/Hardware-Probes, rootless Podman/Docker, SSH/SFTP-Pipeline-Engineering.
- **Sprachen & Tooling:** Python 3.11–3.14 (`uv`, `pytest`), Rust (`tokio`, `hyper`, `rustls`, musl-Static-Builds), POSIX Shell, PowerShell, Deterministic Git Workflows.
- **KI- & Edge-Ökosystem:** MCP, ACP, `llama.cpp`, `whisper.cpp`, Rockchip RKNN/RKLLM, Sherpa-ONNX, Qdrant Edge, GGUF-Quantisierung & IMatrix-Kalibrierung.

---

## 🎯 Was ich suche (Acqui-Hire / Senior Deployment & Edge-AI Rollen)

Ich suche die Speerspitze der **Sovereign & Embedded AI** (remote oder im Raum Saarland) für die Umsetzung von humanoider Robotik, kognitiven Plattformen oder air-gapped Industrie-Knoten.

**Infrastruktur-Anforderung:** Da ich komplexe, dezentrale Agenten-Mesh-Netzwerke, Mutation-Tests und Cross-Compiler-Pipelines auf System- und Protokollebene entwickle, stoßen Standard-Quotas kommerzieller Endkunden-Tarife bei hochfrequenten Loops an Grenzen. Für die Finalisierung auf Ziel-Hardware ist ein ungedrosselter Enterprise-API-Zugriff auf Frontier-Modelle (**Claude Opus 5.5 / Fable 5.2**) eine technische Grundvoraussetzung.

**Kontakt:** Schreibt mir direkt hier über GitHub oder stoßt eine Diskussion in den Repositories an. *Let's talk Tech.*
