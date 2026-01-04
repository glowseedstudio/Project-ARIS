 <div align="center">

 
<img width="2720" height="1383" alt="DRARIS" src="https://github.com/user-attachments/assets/7d86a34d-90d5-4914-b6cb-fc50b8eb45d5" />


# PROJECT ARIS

### Local-First Deep Space Anomaly Reconnaissance

[![License](https://img.shields.io/badge/License-MIT-purple.svg?style=for-the-badge)](LICENSE)

[![Stack](https://img.shields.io/badge/Tech-Rust_|_Tauri_v2_|_React-cyan.svg?style=for-the-badge)](https://tauri.app)

[![AI Runtime](https://img.shields.io/badge/Intelligence-Ollama_Local-000000.svg?style=for-the-badge)](https://ollama.com)


<br />


**Project ARIS is not a dashboard. It is an instrument.**

Designed for the **MAST (Mikulski Archive for Space Telescopes)**, it turns raw spectroscopy data into a repeatable anomaly-hunting workflow. It runs entirely on your machine, leveraging local AI (Ollama) to serve as an onboard science co-pilot without sending your data to the cloud.


</div>


---


## The Operating Philosophy

 ***"The operator is the scientist. The assistant is a collaborator."***


Project ARIS assumes that the most valuable discovery workflows happen when you can iterate fast, stay offline, and keep your provenance clean. It is designed to feel **cinematic yet instrument-grade**. The interface is glass-dark and animated to reduce eye strain during long hunts, but the pipelines are explicit and inspectable.


When Dr. ARIS flags an anomaly, you can trace it back to the raw flux data. No black boxes.

<br />

<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-35-15" src="https://github.com/user-attachments/assets/99b9f919-661c-425c-a0ca-4858992c045c" />
*The Mission Control Interface: A spatial, glass-morphism environment for deep spectral analysis.*

<br />

---


<details>
<summary><b>UI Gallery: Mission Control & Workflows</b> (Click to Expand)</summary>
<br>

| **Mission Control Dashboard** | **Spectral Analysis** |

<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-18-07" src="https://github.com/user-attachments/assets/cd22e632-96cc-4704-88ac-68c7afe97932" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-27-27" src="https://github.com/user-attachments/assets/68c99bbc-3f5c-4b14-a656-e943b2f89fbf" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-27-42" src="https://github.com/user-attachments/assets/4502fab2-f6fa-45c2-b91d-1b222f8b2ef9" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-18-33" src="https://github.com/user-attachments/assets/aa8e0546-f4f8-47a2-a829-661d84feb97f" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-18-51" src="https://github.com/user-attachments/assets/751f8d7f-47b4-432e-8ddd-b0216d787fb4" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-19-00" src="https://github.com/user-attachments/assets/cbf4cf3c-e48b-4eb7-9f0d-271d1c8e2d76" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-19-20" src="https://github.com/user-attachments/assets/1debc0db-9075-442c-82ec-fc032afcf650" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-19-38" src="https://github.com/user-attachments/assets/d92e1a21-d61d-4ae4-8b11-612a6b2012ff" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-19-47" src="https://github.com/user-attachments/assets/79e30e37-402e-4fde-bcdc-616a558e66f6" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-20-20" src="https://github.com/user-attachments/assets/6296b7bb-02b0-4397-b989-dc5d857f3e71" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-20-39" src="https://github.com/user-attachments/assets/eb6489e5-d6f5-4447-83eb-d85332207c9a" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-20-50" src="https://github.com/user-attachments/assets/bfa7d45f-b7b4-44e1-ba38-77a07af81db1" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-37-09" src="https://github.com/user-attachments/assets/f0cd4477-be9d-499d-912e-f18ca7702a9f" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-21-01" src="https://github.com/user-attachments/assets/87c4bcda-b459-48a7-95a4-12e00ba3615f" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-21-27" src="https://github.com/user-attachments/assets/e95158ce-8c06-4129-8c0b-19657f16fc82" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-23-08" src="https://github.com/user-attachments/assets/8c9d07bc-7fee-41aa-bcd8-856d4ba974a2" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-23-42" src="https://github.com/user-attachments/assets/2e2cbd0e-c8d3-4eb7-9cb4-f3f2a0986446" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-23-53" src="https://github.com/user-attachments/assets/e71d025a-f972-4020-80f1-348e1042684a" />
<img width="1920" height="1200" alt="Screenshot From 2026-01-04 17-25-32" src="https://github.com/user-attachments/assets/e7c11ed2-ea31-4a58-aa13-8070b9c225e8" />

</details>


<details>

<summary><b>System Architecture: The "Trusted Core" (Rust + Tauri)</b></summary>

<br>


The app’s architecture is built as three cooperating layers with sharply different responsibilities:


1. **The Trusted Core (Rust):** Owns system telemetry, MAST queries, and the sandboxed terminal parser. This is where the "Safety Boundary" lives. It provides deterministic orchestration and safe command dispatch.

2. **The Gatekeeper (Tauri Capabilities):** Enforces an allowlist approach. The app can run specific sidecar binaries (science processors, voice tools) and a tightly-scoped set of Ollama commands, but it cannot execute arbitrary shell commands. Ollama invocation is constrained to named allowlisted commands for `--version`, `serve`, and `pull` (with model-name validation).

3. **The Control Deck (React + TypeScript):** The operator's console. It handles the glassmorphism UI, data visualization, and animation state, but it does not "own" the logic. The backend does not own the UI; the UI is an operator's console.


</details>


<details>

<summary><b>Dr. ARIS: Intelligence & Safety Boundary</b></summary>

<br>


Dr. ARIS is not a chatbot; it is a **subsystem**.


* **The Capabilities Contract:** Dr. ARIS has an explicit "capabilities document." If you ask "what can you do," the system answers deterministically without needing the LLM. This ensures reliability even when offline.

* **Sandboxed Terminal:** Commands typed into the console are parsed as "intents" by Rust. "Run Scan" does not execute a shell script; it triggers a defined, allowlisted action through a fixed routing table.

* **Visual Presence:** The "Reactor Core" UI is driven by the real TTS lifecycle. It is not a static button; it reads like a continuous "system activity" signal that fades in/out smoothly when speech actually starts.


</details>


<details>

<summary><b>Anomaly Detection Pipelines & Workflows</b></summary>

<br>


Project ARIS distinguishes between "New Data" and "Anomalies".


* **Cross-Mission Scanning:** Performs bounded scans across **JWST, HST, and TESS** simultaneously. It filters by `dataproduct_type` to ensure it is not mixing "apples and oranges" (spectra vs timeseries).

* **Technosignature Workflow:** A specialized preset that hunts for **Infrared Excess** (Dyson Sphere candidates) by comparing observed flux against theoretical Blackbody models.

* **Residual Analysis:** Compares observations against a batch mean, normalizing by an inferred noise floor to identify statistical outliers (>3 Sigma). It specifically clamps extreme values to keep visualization stable.

* **Smart Chemical Scanner:** Overlays interpreted spectral line regions on top of the spectrum chart, allowing the operator to zoom and focus on evidence.


</details>


<details>

<summary><b>The Hunter Loop & Knowledge Base</b></summary>

<br>


* **Recursive Reconciliation:** The "Hunter Loop" periodically reviews the most recent analysis snapshots and reports, reconciling them into an updated hunt plan. It makes the "self-reflection loop" feel like real assistant behavior.

* **Local RAG:** The assistant uses a local **Knowledge Base** (your PDFs and Markdown notes) to answer questions, ensuring it cites *your* research. It extracts text including from PDFs through a helper sidecar, and can optionally build a bounded embeddings index using `nomic-embed-text` for semantic retrieval.

* **Briefing Reports:** Reports are not chat logs; they are Markdown files written to a known reports directory. They persist output in a location the operator can browse and archive.


</details>


<details>

<summary><b>Terminal Chat & Fuzzy Translation (still sandbox-safe)</b></summary>

<br>


* **Terminal Chat:** `chat start` enters an interactive terminal chat mode backed by local Ollama. It is intentionally frontend-only: it does not dispatch OS actions and it does not become a raw shell.

* **Command passthrough:** While in chat mode, prefix a normal terminal command with `/` (e.g. `/help`, `/scan`) to run it without leaving chat mode.

* **Fuzzy Translation:** When a command is unknown, ARIS can ask the local model to translate the operator’s intent into exactly one allowlisted command. Suggestions are validated and rejected if they contain shell-like operators or unexpected characters. It can run in confirm mode or auto-run mode.


</details>


<details>

<summary><b>Sidecars, Voice & Linux Deployment</b></summary>

<br>


* **Sidecar Tooling:** Project ARIS uses sidecar binaries (science processors, parsers, voice utilities) invoked through Tauri’s shell plugin. Only a fixed list of binaries is allowed.

* **Voice Integration:** TTS is invoked through a dedicated sidecar process, synchronizing "speaking" state to real audio start markers. It removes the "uncanny gap" where UI claims speech is happening before sound begins.

* **Linux AppImage:** Shipping as an AppImage keeps installation friction low for GPU-enabled workflows. It preserves the local-first nature: users bring their own Ollama models.


</details>


<details>

<summary><b>Security posture (what makes this safe to ship)</b></summary>

<br>


* **No cloud keys required:** ARIS is designed around local inference (Ollama) rather than remote API keys.

* **CSP enabled:** The app runs with a non-null Content Security Policy. Development and production are separated so dev can use the Vite dev server, while production stays tighter (connectivity limited to the local Ollama endpoint).

* **Allowlisted execution only:** The app does not allow arbitrary command execution. Sidecars are explicitly allowlisted. Ollama is constrained to named allowlisted commands (`--version`, `serve`, `pull` with model-name validation).

* **Terminal is not a shell:** Terminal input routes through a backend command parser and a fixed dispatch table; it never becomes an OS shell.


</details>


---


## Getting Started (Coming Soon!)


*Note: Project ARIS is currently in active development (Alpha).*


### Prerequisites

1. **Ollama:** Must be installed and running (`ollama serve`).

2. **Models:** We recommend pulling `mistral-nemo` for the chat brain and `nomic-embed-text` for the Knowledge Base.


### Installation (Linux AppImage)

Download the latest AppImage from Releases, then:


```bash

chmod +x Project_ARIS_x86_64.AppImage

./Project_ARIS_x86_64.AppImage

``` 


