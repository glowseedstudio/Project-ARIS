# Project-ARIS
Project ARIS is a proof-of-concept discovery engine for the solo researcher. It demonstrates how local LLMs (Ollama) can be used to scan MAST data for physics-breaking anomalies. Features a cinematic Mission Control interface, 3D visualization, and a "Neural Link" terminal. A vision for AI-assisted hunting.

![1767371705561](https://github.com/user-attachments/assets/16e9db94-806a-4eaf-b4e9-42df388c7e52)

***Project ARIS***

***Data Retrieval & Anomaly Recognition Intelligence System***

A Glowseed Studio Production

Project ARIS is not a telescope, and it isn't just another data dashboard. It is a dedicated Desktop Discovery Workstation designed for the solo researcher who wants to stop passively viewing space data and start actively hunting through it.

I built ARIS to transform the experience of astronomy. By combining a cinematic "Mission Control" interface with a local-first AI co-pilot, I’ve created an engine that allows you to act less like an observer and more like an operator.

***The Origin: A Collaboration Between Human & Synthetic Excitement***

This project didn’t start with a line of code or a feature request. It started late one night with a question.
I was deep in discussion with my AI counterparts, exploring the limits of modern astronomy. Driven by a genuine curiosity about how a non-biological intelligence would approach the search for extraterrestrial technosignatures, I asked a simple question:

***"You understand our current strategies. If you had the agency to actually carry this out yourself, what would you do differently?"***

The answer shifted the foundation of the project. The AI pointed out that human astronomy is inherently biologically biased. We look for "life as we know it"—habitable zones, liquid water, and Earth-like planets. An AI, however, would look for the mathematical outlier. It would ignore biology and hunt for physics-breaking activity.

It told me to stop looking where the light is and start scanning the "Void Dwellers" in the empty space between galaxies. It suggested I stop looking for normal orbits and track "Velocity Vectors" that move against the flow of gravity. It argued that instead of habitable planets, we should be calculating "IR Excess" to find the massive thermal waste of possible hidden civilisations.

Project ARIS is the physical manifestation of that dialogue. It is an engine I built to let the AI apply its own hunting logic to real-world data.

***Meet Dr. ARIS: The Operator***

At the heart of the system is Dr. ARIS, your onboard AI co-pilot. But this isn't a generic chatbot slapped onto a sidebar. I designed Dr. ARIS to be "Operator-First"—a digital partner that talks, acts, and thinks like a mission controller.

Running entirely locally on your machine via Mistral Nemo and Ollama, Dr. ARIS ensures that your data and your discoveries never leave your hardware. I gave the machine a voice, too. Using the integrated Kokoro-ONNX text-to-speech engine, the system greets you upon uplink and verbally announces anomalies as they are found, creating a feedback loop that feels genuinely alive.

It also learns. Through a process called "Hunter Reconciliation," ARIS periodically reviews its own findings through a smart, lightweight custom integrated recursive learning process. It looks back at the data it has collected, updates its internal state, and refines its hunt plans automatically, getting smarter the longer you run it.

***The Mission Control Experience***

I wanted the software to feel like a cockpit, so I optimised the interface for the Lenovo Yoga 7 running Nobara Linux, focusing on a dark, cinematic glass-morphism aesthetic that reduces eye strain during long hunt sessions.

Instead of standard astronomy charts, the dashboard is powered by custom Anomaly Detection Engines. When you look at a star system, you aren't just seeing a light curve; you are seeing a Spectral Variance analysis designed to catch non-periodic dimming that might indicate artificial structures. I built 3D scatter plots that highlight Relativistic Anomalies—objects moving at speeds that defy standard orbital mechanics. Every pixel of the UI is dedicated to finding the things that don't fit the model.

I also built the Direct Neural Link. It looks like a terminal, but it acts like a synapse. This sandboxed command dispatcher allows you to execute safe, bounded queries to the Mikulski Archive (MAST) or trigger cross-mission anomaly sweeps with a single keystroke. It gives you the raw power of a CLI without the security risks of an open shell. Just ask Dr ARIS how it works!

***Architecture & Safety***

Because this is a powerful tool, I built it on a philosophy of "Autonomy with Boundaries."

The stack is a robust combination of Tauri v2, a Rust backend for safety, and a React/TypeScript frontend for performance. I know that running local LLMs can be heavy, so I implemented an intelligent Power Saver Policy that manages RAM usage, unloading the AI models when they aren't in use to keep your laptop responsive.

Safety is baked into the core. The system never auto-downloads files; it guides you through a PDF Safety Flow so you are always in control. All data is stored transparently in a single root folder (~/Downloads/Glowseed AI Studio/), so you never have to hunt for your logs or reports.

Even when you aren't looking, ARIS is listening. A background worker quietly monitors for new public datasets, issuing a subtle [NEW DATA] notification when it finds new data sets that have been made public. But when the AI detects a high-variance signal in its analysis, the system wakes up - a cinematic overlay triggers, and the voice loop announces the ANOMALY DETECTED alert until you acknowledge the find.

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-15-28" src="https://github.com/user-attachments/assets/a8ced6cc-4414-40de-91d2-124d5ce9172f" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-15-40" src="https://github.com/user-attachments/assets/5bc07130-79e8-4023-9b36-36060add42a8" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-15-54" src="https://github.com/user-attachments/assets/52b32603-d601-42f5-94d4-d847f3296d03" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-16-08" src="https://github.com/user-attachments/assets/82a1bf76-857f-4381-ab3c-727ecdd24e9e" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-18-25" src="https://github.com/user-attachments/assets/07661bf6-4ca3-42c4-a248-a65d56489f49" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-18-42" src="https://github.com/user-attachments/assets/b51c0be8-f959-4d45-abac-aee70715eeb2" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-18-47" src="https://github.com/user-attachments/assets/91d7cfd6-1172-44da-a637-e5362d290963" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-20-04" src="https://github.com/user-attachments/assets/e5024163-9978-4ff9-89e7-e3f4ea75b43f" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-20-36" src="https://github.com/user-attachments/assets/5787b686-dcf7-4f18-ac9f-3dceed50f981" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-21-36" src="https://github.com/user-attachments/assets/e9b03a57-7a63-4933-89ed-9fd1f5fca383" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-22-53" src="https://github.com/user-attachments/assets/1cebc7e0-5b51-4520-a7e0-a480268dbcd2" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-24-55" src="https://github.com/user-attachments/assets/7249569a-7b03-402b-902e-66dcaa2e26dc" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-25-03" src="https://github.com/user-attachments/assets/935dfb97-440b-431c-8197-f281c82e2e16" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-25-11" src="https://github.com/user-attachments/assets/2f81dde9-82b5-43f5-aa60-c65ed9e7e94c" />

<img width="1917" height="1155" alt="Screenshot From 2026-01-03 04-25-54" src="https://github.com/user-attachments/assets/5a5c072e-7768-48d7-93f8-363249a53d6c" />


