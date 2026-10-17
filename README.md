# Hi, ich bin Smilez1985 🛠️

**Systems & Platform Architect | Local-First AI Infrastructure | DevSecOps & Integration**

Ich bin Fachinformatiker für Systemintegration (FiSi) aus dem Saarland. Ich schreibe keine akademischen Whitepaper über theoretische Cloud-Modelle – ich baue die schockresistente, air-gapped Infrastruktur, die Large Language Models und RAG-Systeme stabil, asynchron und sicher auf echte Edge-Hardware (ARM, NPUs, Handhelds) bringt.

In meinem privaten Homelab betreibe ich ein heterogenes Mesh-Netzwerk aus autonomen KI-Agenten auf modifizierten OpenMinis (Android Custom-ROMs mit Root/Shizuku und Linux-Knoten). Mein Fokus liegt auf digitaler Souveränität: **KI unabhängig von Big-Tech-Serverfarmen, lokal optimiert, asynchron gekoppelt und kryptografisch gehärtet**.

Ich kenne nicht jede CLI-Option von Docker auswendig. Ich nutze LLMs hocheffizient als meinen Code-Monkey für die reine Syntax. Meine Stärke liegt in der Systemarchitektur und der logischen Absicherung. Ich weiß, wie man fehlerhafte SDKs in Containern isoliert, wie man asynchrone Kommunikationsschleifen über Netzwerk-Klingeln baut und wie man RAG-Systeme framework-agnostisch aufsetzt. Den Code dazu lasse ich die KI schreiben, aber ich kontrolliere, auditiere und strukturiere das System nach harten Enterprise- und Security-Vorgaben.

---

## 🚀 Mein Core-Ökosystem (Einsatzbereit für Edge & Robotik)

Ich entwickle modulare, aufeinander abgestimmte Plattformen, die das Zusammenspiel zwischen Hardware und Intelligenz abstrahieren und absichern:

### 1. 🏗️ [LLM_Cross-Compiler_Framework]([https://github.com/Smilez1985/LLM_Cross-Compiler_Framework])
*Zähmt das Chaos proprietärer Hardware-SDKs.*
- **Was es tut:** Kapselt fehleranfällige und inkompatible Compiler-Toolchains der Chiphersteller (wie Rockchip/RKNN) vollständig in isolierten Docker-Containern (Air-Gapped-Builds ohne Netzwerkeingriff).
- **Die Technik:** Automatisiert die Pipeline von Hugging-Face- oder lokalen Gewichten über GGUF (CPU/llama.cpp) und RKLLM/RKNN (NPU) bis zum deterministischen Deployment via systemd-Units direkt auf dem Ziel-SBC. Unterstützt Smart Calibration via Importance Matrix (IMatrix).
- **Status:** Produktionsreifes Fundament (>1.220 Commits), modularer orchestratierter Monolith mit robuster Test-Suite.

### 2. 🧠 [rag4ll] (in Entwicklung / noch Privat)
*Markdown-first, framework-agnostische RAG-Memory für dezentrale Agenten.*
- **Was es tut:** Gibt KIs ein langlebiges Gedächtnis auf block-bewusster Markdown-Basis (erhält Heading-Paths und Code-Grenzen), das die Laufzeit des einzelnen Agenten überlebt.
- **Die Technik:** Nutzt eingebettete Vektordatenbanken (Qdrant Edge) und ein servergesteuertes Lese-Gate als kryptografisch gesicherten (PSK-Seal) Inter-Agent-Message-Bus. Nachrichten laufen erst ab (TTL), nachdem das Ziel sie nachweislich gelesen hat.
- **Optimierung:** Integriert ein Lazy-Load-Embedding- und Rerank-Sidecar, das GPU-Ressourcen im Leerlauf automatisch freigibt.

### 3. 🔔 [woa-l (Wake on Agent Loop)](in Entwicklung / noch Privat)
*Asynchrones, batteriesparendes Event-Routing für autonome Schleifen.*
- **Was es tut:** Löst das Problem, dass KIs zwischen zwei Nachrichten nicht als Prozess existieren. Statt teure, synchrone Cloud-Dauerschleifen laufen zu lassen, etabliert `woa-l` ein ereignisgesteuertes Aufweck-Protokoll.
- **Die Technik:** Eine winzige HTTP-Klingel in der Agenten-Sandbox lauscht auf diskrete JSON-RPC-Signale (MCP über HTTP). Sie hängt den Reiz als Prompt an die aktive Session an, reaktiviert den Agenten für exakt einen Turn und legt den Prozess sofort wieder schlafen.

---

## 🛡️ Mein Security- & FiSi-Mindset

Weil ich mein eigenes System permanent im harten Alltagstest (Dogfooding) auditiere, weiß ich, dass autonome Agenten mit Systemrechten tickende Zeitbomben sind. Ich baue keine naiven API-Wrapper. Ich integriere:
- Strikte Sandbox-Kapselung ohne privilegierte Root-Rechte beim Modell-Kompilieren.
- Automatisierte Image-Vulnerabilitiy-Scans (Trivy) direkt in der Pipeline.
- Umfassendes Capability-Gating und textbasiertes Input-Sanitizing, um Prompt-Injections auf Betriebssystemebene architektonisch zu blockieren.

---

## 🛠️ Tech-Stack in der Praxis

- **Infrastruktur:** Docker / Container-Isolation, Linux-Systemadministration (Debian/Ubuntu/Alpine), systemd-Automation, Udev/Hardware-Probes, SSH/SFTP-Pipeline-Engineering.
- **KI Ecosystem:** Model Context Protocol (MCP), GGUF / RKLLM / RKNN Quantisierung, Qdrant Edge, llama.cpp-Kompilierung.
- **Tooling & Methoden:** `uv` Paketmanagement, Deterministic Git Workflows, Air-Gapped Security Architecture.

---

## 🎯 Was ich suche (Acqui-Hire / Senior Deployment Rollen)

Ich suche keine klassischen First-Level-Tickets oder theoretische Cloud-Architektur-Rollen. Ich suche die Speerspitze der **Sovereign & Embedded AI** – remote oder im Raum Saarland. 

Wenn Ihr Team humanoide Roboter, kognitive Plattformen oder Air-Gapped Industrie-Knoten baut und jemanden braucht, der die Software-Visions-Blase sicher auf den physikalischen Ziel-Chip bringt, bin ich Ihr Mann. Ich bringe meine drei Core-Infrastrukturen als einsatzbereites geistiges Eigentum direkt in Ihr Ökosystem ein.

**Kontakt:** Schreibt mir direkt hier über GitHub oder stoßt eine Diskussion in den Repositories an. Let's talk Tech.
