FM-1 Bridge – Technical Research
1. Project Objective

FM-1 Bridge aims to make M-VAVE FM-1 synthesizer firmwares available as WebCLAP instruments in openDAW.

The project should support multiple compatible firmware projects rather than just one synthesizer.

2. Existing Projects
VIBE FM
Website: https://thefirmwarehub.com/
SDK: https://github.com/Vibe-FM-SDK/vibe-fm-sdk
Provides a common environment for FM-1 firmware ports.
Supports browser and desktop DAW workflows.
openDAW WebCLAP
Repository: https://github.com/andremichelle/open-webclap
Documentation: https://opendaw.studio/manuals/devices/audio/wclap
WebCLAP plugins run as WebAssembly modules inside openDAW.
FM-1 Firmware Converter
Website: https://thefirmwarehub.com/convert/
Converts compatible open-source FM-1 firmwares into VIBE FM instruments.
3. Technical Architecture

Proposed architecture:

FM-1 Firmware Source | v VIBE FM SDK / Firmware Port | v WebCLAP Integration Layer | v WebCLAP Bundle | v openDAW

This architecture is preliminary and requires a feasibility test.

4. Important Technical Questions
Can the VIBE FM SDK be integrated with the WebCLAP ABI?
Can existing converted firmware engines be reused?
How can MIDI input be mapped?
How can firmware parameters be exposed to openDAW?
How should presets and project state be saved?
How can different firmware licences be respected?
5. First Prototype

Target instrument: OberVave FM-1.

Initial requirements:

Load successfully in openDAW.
Produce audio.
Receive MIDI notes.
Expose basic synthesizer parameters.
Save and restore plugin state.
6. Development Principles
Open-source development.
Respect original firmware authors and licences.
Avoid unnecessary duplication of existing code.
Support multiple firmware projects.
Keep the integration modular and maintainable.
7. Project Status

Current phase: Research and feasibility.

No working WebCLAP integration has been completed yet.

8. Next Milestone

Build a minimal WebCLAP proof of concept and investigate integration with the VIBE FM SDK.
