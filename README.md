Recluse
Overview
Recluse is an anti-burnout matchmaking platform designed specifically for introverts, shut-ins, and high-focus professionals. Traditional dating apps prioritize physical proximity, endless swiping, and high-pressure offline meetups. Recluse flips the model: it assumes you want to stay exactly where you are.

By facilitating rich, low-friction "virtual-first" interactions, the app provides a safe, highly controlled environment for socially anxious or deeply introverted individuals to forge meaningful romantic connections without draining their social batteries.

Core Features
Virtual-First Dates: In-app integrations that allow you to share an activity without forced small talk. Sync a movie, launch a localized co-op game session, or open a shared whiteboard to collaborate on a project.

Social Battery Limits: To prevent decision fatigue and swiping burnout, Recluse limits users to viewing 5 highly curated matches per day.

The "Deep Work" Toggle: A specialized status mode for workaholics. It pauses your profile visibility and pauses match timers so you can disappear into a two-week sprint without the anxiety of ghosting someone.

Communication Menus: Profiles feature a "Communication Preference" matrix. Let potential matches know if you prefer long-form asynchronous messages, parallel play (being on a call while doing different things), or text-only chats.

Technical Architecture
The infrastructure of Recluse prioritizes high performance, stability, and absolute privacy for its users' most intimate communications.

Backend Engine: The core microservices are written in Rust to guarantee memory safety and handle highly concurrent WebSocket connections seamlessly.

Real-Time Data Streaming: Low-latency features like in-app screen sharing, voice chat, and synchronized media playback are handled by highly optimized Zig modules, keeping server-side resource overhead extremely low.

Privacy-First Content Moderation: Instead of sending chat logs to external corporate APIs to scan for abuse, Recluse utilizes an embedded local AI pipeline. By tying into Ollama, the platform runs small, fast language models directly on the host server to moderate content autonomously, ensuring no third party ever reads user messages.

Build Instructions
Prerequisites:

Rust toolchain (latest stable)

Zig compiler (v0.11+)

Ollama environment configured for the moderation daemon

Steps:

Clone the repository to your local machine.

Initialize the isolated database schema.

Build the Zig real-time media streaming libraries.

Compile the Rust backend using cargo build --release.

Start the Ollama moderation service before launching the application server.
