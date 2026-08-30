# Hi, I'm Tair

Everything below is in private repos, so no links. Happy to walk you through any of it though!

## VividForms

I build software for VividForms, a robotic fabrication studio in Almaty that does robotic 3D printing and ultra-high-performance concrete for architectural and sculptural work.

**Brodyaga.** A measuring system for the workshop, built with a small team. A rover with an 11-camera rig localizes against a map of about 340 ArUco markers, built by photogrammetry with COLMAP and anchored to total-station survey points. Ceiling projectors indicate work positions to the sculptor. Localization runs as a sparse bundle adjustment that jointly solves camera intrinsics, rig extrinsics, body poses, and the marker map against surveyed priors.

I work on the accuracy side: an observation-noise model based on each marker's apparent size in pixels, posterior covariance computed from the Gauss-Newton Hessian, and corner-detection corrections (AprilTag refinement accepted only within 15 px agreement with the subpixel detector, and averaging of burst captures while the rover is stationary). Placement consensus between independent cameras is currently about 2 cm at 1.6 px reprojection error. Calibration changes are evaluated on held-out positions before being adopted.

**Workshop AR viewer.** A WebXR prototype that places CAD models on the shop floor at 1:1 scale through Quest 3 passthrough. Uses the WebXR device API with hit-test placement and three.js, served from a small Python script on the local network. Around 650 lines of code, no build step, and nothing installed on the headset.

## Amanuensis

A Mac app for drafting prose in your own voice. Electron and React frontend, with a Python sidecar connected over the Agent Client Protocol. It builds a persona from your writing samples, then drafts, critiques, and revises using a different model for each pass, configured in a routing file. Supports local generation through MLX, including LoRA fine-tuning on your own samples. The voice-match score is validated with a leave-one-passage-out eval (0.986 ROC AUC on the reference corpus, documented as an upper bound). The eval suite includes a local implementation of Fast-DetectGPT, audited against the RAID benchmark. User-facing claims are tracked in a ledger with their measurement status. Drafts stay on the machine.
