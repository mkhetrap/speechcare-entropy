# SpeechCARE Entropy Integration (UI Prototype)
This repository contains the entropy-graph integration work extracted from the SpeechCARE interface prototype.
## What is included
### 1) Entropy integration script
- `interface/generate_interface.py`
- This script contains the core logic used to generate the report HTML and entropy section behavior, including:
  - entropy plot display wiring
  - second audio player under entropy
  - synchronized playback behavior
  - moving red playhead over the entropy graph
  - real-time transcript display variants
### 2) Preview variants (AD / MCI / Control)
- `preview_pages/ad_preview_v1.html`
- `preview_pages/ad_preview_v2.html`
- `preview_pages/ad_preview_v3.html`
- `preview_pages/mci_preview_v1.html`
- `preview_pages/mci_preview_v2.html`
- `preview_pages/mci_preview_v3.html`
- `preview_pages/control_preview_v1.html`
- `preview_pages/control_preview_v2.html`
- `preview_pages/control_preview_v3.html`

These are static preview outputs showing three UI versions per cohort.
## Version meaning
For each cohort (`ad`, `mci`, `control`):
- **v1**: cumulative transcript box only (no moving single-word ticker)
- **v2**: cumulative transcript box + moving single-word ticker
- **v3**: moving single-word ticker only (large transcript box hidden)
## Entropy audio/playhead behavior
All included preview versions support:
- a dedicated entropy audio bar under the graph
- one-at-a-time playback handling between top and entropy players
- red playhead synced to entropy timeline
- tuned spacing between entropy graph and soundbar (`margin-top: -10px` in `.entropy-audio-under-plot`)
## How to use this repo
This repo is meant as a focused handoff for porting entropy behavior into a live codebase.
Recommended process:
1. Review `interface/generate_interface.py` for source implementation.
2. Use `preview_pages/*_v1/v2/v3.html` as visual reference and behavior validation.
3. Port the entropy section styles/scripts into the target live template.
## Notes
- These preview files are static HTML snapshots for review/testing.
- They rely on embedded content generated from the original project pipeline.
- This repo intentionally excludes unrelated project files to keep the entropy changes isolated.
