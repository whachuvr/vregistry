# VRegistry

**VR Mod Implementation Registry**  
Built by **whachuvr**

> **Mods are the evidence. Patterns are the knowledge.**

VRegistry is a source-reviewed knowledge base focused on how flatscreen games are converted into fully interactive VR experiences.

Rather than simply cataloging VR mods, VRegistry studies their source code and extracts reusable implementation methodology covering rendering, tracking, motion controls, interaction, IK, weapons, UI, locomotion, haptics, engine integration, and other VR systems.

The goal is to make proven VR modding techniques easier to discover, compare, and reuse — by developers and AI coding tools.

---

## What VRegistry Contains

VRegistry contains **1,200+ implementation references** extracted from open-source VR mods, VR frameworks, source ports, engine integrations, and runtime hooks.

Entries are organized around VR subsystems including:

- Architecture
- Stereo Rendering
- Frame Timing
- Camera Tracking
- Input
- Hands / Motion Controls
- Body IK
- Weapon Aiming
- Melee Combat
- Physical Interaction
- Gesture Interaction
- UI Projection
- Locomotion
- Vehicles
- Multiplayer
- Haptics

Each implementation pattern is intended to answer a practical question:

**How was this VR feature actually implemented?**

---

## Source-Reviewed Implementation Patterns

VRegistry is built around implementation evidence.

Source audits examine real VR mod code and extract techniques such as:

- OpenXR / OpenVR runtime integration
- Vulkan, DirectX, and OpenGL stereo rendering
- Alternate-eye and native stereo rendering
- Camera ownership and HMD tracking
- Roomscale player movement
- Motion-controller input translation
- Native game input injection
- Tracked weapon aiming
- Two-handed weapon handling
- Physical melee
- Physical interaction
- Full-body and arm IK
- World-space UI
- VR HUD conversion
- Native gameplay function reuse
- Engine hooks and injection architecture
- Frame synchronization
- Haptic translation
- Source-port VR architecture
- Runtime compatibility techniques

Small implementation details are kept within the supporting audit when they belong to a larger technique rather than being treated as separate patterns.

---

## Projects Studied

VRegistry includes implementation knowledge from projects across many different engines and VR conversion approaches.

Examples include:

- DOOM (2016) / KHARVOX
- RazeXR / Duke Nukem 3D
- Dishonored VR
- HaloCEVR
- Majora's Mask VR
- REFramework
- Left 4 Dead 2 VR
- Cyberpunk 2077 VR
- Dead Island 2 VR
- Oblivion Remastered VR
- Subnautica 2 UEVR
- UEVR projects
- Native engine hooks
- Source-port VR conversions

The registry focuses on the reusable engineering techniques demonstrated by these projects.

---

## Explore by Subsystem

The registry can be filtered by:

- VR subsystem
- Engine
- Rendering / VR API
- Integration method
- Entry type
- Project
- Search terms

Selecting a subsystem makes it possible to compare how completely different VR mods solve the same technical problem.

For example, **Weapon Aiming** can contain approaches based on:

- native muzzle replacement
- gameplay trace rewriting
- temporary native actor rebasing
- controller-driven raycasts
- existing engine aim systems
- framework-level weapon transforms

This makes VRegistry useful as more than a list of mods — it becomes a reference for known VR implementation strategies.

---

## Export for LLM

VRegistry can generate focused implementation context for use with an LLM or coding agent.

A **subsystem must be selected before exporting**.

This prevents the entire registry from being dumped into context and keeps the export focused on the technical problem being solved.

Additional filters can narrow the export further by engine, API, integration method, project, or search query.

Example:

```text
Subsystem: Weapon Aiming
Engine: Unreal Engine
Integration: Native Hook
```

The resulting export contains relevant implementation patterns and supporting source-audit information.

---

## Build Routes

VRegistry groups VR development approaches into broad implementation families:

- Unreal Engine + UEVR
- Unity + Managed Mod
- Source Engine + Native Hook
- OpenXR / OpenVR + Native Hook
- DirectX + Native Runtime Hook
- API + Rendering Layer
- Source-Level + Engine Fork
- id Tech / Quake + Source Port

These are intended to help developers identify implementation patterns relevant to the type of VR mod they are building.

---

## Source Auditing

VRegistry distinguishes between what is actually supported by source code and what is not.

An audit may explicitly identify that a project does **not** implement a subsystem.

For example:

```text
Body IK: Not implemented
Vehicle VR controls: Not implemented
VR multiplayer pose replication: Not implemented
```

Commented-out systems, dormant experiments, documentation-only claims, and unavailable source are not presented as active implementation evidence.

If only part of a system is visible in the available source, the registry records that boundary.

---

## Contributing

VR mod authors and developers can submit projects for review through VRegistry.

### Public Repository

Provide a public source repository and information about the project.

Useful repositories may contain implementations involving:

- rendering
- tracking
- controls
- IK
- weapons
- interactions
- locomotion
- UI
- multiplayer
- haptics
- engine integration

### Private Source

Closed-source developers may also submit source for private review.

Private source code itself is not intended to become a public registry artifact. Public entries should contain reusable implementation methodology rather than proprietary source files, credentials, or private files.

Authors can specify additional privacy requirements when submitting a project.

---

## Design Philosophy

VRegistry is designed around a few simple principles:

**Source over speculation.**

Implementation claims should be grounded in source code or clearly identified supporting documentation.

**Patterns over project summaries.**

Knowing that a VR mod exists is less useful than understanding how its systems work.

**Reusable methodology over trivia.**

Not every interesting implementation detail deserves its own registry entry. Closely related details belong underneath stronger reusable patterns.

**Preserve native game systems when possible.**

Many of the most useful VR techniques in the registry demonstrate ways of feeding VR tracking into existing gameplay systems instead of rebuilding those systems from scratch.
