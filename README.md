# Hi, I'm Tair

## What I'm working on now

This work is in private repos, so no links. Happy to walk through any of it.

**Amanuensis.** A Mac app for drafting prose that sounds like you, not like a model. Electron and React up front; underneath, a 28k-line Python sidecar that talks to the app over the Agent Client Protocol, the same way coding agents do. It builds personas from your writing samples, then drafts, critiques, and revises with a different model per pass. Model routing is data, not code: Claude as the voice engine, a cheaper separate model as the critic, and an optional local MLX engine with LoRA fine-tuning on your own prose.

The measurement side is the part I care about. The voice gauge scores 0.986 ROC AUC on a leave-one-passage-out split separating same-author from different-author text, and the eval docs treat that as an upper bound, since the corpus is the easiest case stylometry ever gets. The eval suite also implements Fast-DetectGPT locally and audits it against the RAID benchmark. Every claim the app makes has a row in a claims ledger with its measurement status, and the count of open unmeasured overclaims is zero. Drafts never leave your machine.

**Brodyaga.** A camera rover for a sculpture workshop, built with a small team. Eleven cameras on a rig, about 340 ArUco markers on the walls, mapped by Canon photogrammetry through COLMAP and anchored to total-station survey crosses, and ceiling projectors that show the sculptor where to work next. Localization is a sparse anchored bundle adjustment that jointly solves camera intrinsics, the eleven rig extrinsics, per-stop body poses, and the marker map against surveyed priors.

My part is accuracy. I fit the observation-noise model, sigma as a function of a marker's apparent size in pixels with a per-camera factor, so a camera aimed at a far wall isn't penalized twice. I compute posterior covariance from the robust Gauss-Newton Hessian, so every pose ships with error bars in millimeters and degrees. And I fixed corner detection: AprilTag refinement is accepted only where it agrees with the subpixel detector within 15 px, and burst capture medians corners across a volley while the rover stands still. Independent cameras currently agree on placement to about 2 cm at 1.6 px reprojection error. A calibration change only ships if it wins on held-out positions; the last candidate lost, 16.2 mm against the incumbent's 12.8, and was rejected.

**Workshop AR viewer.** A weekend-sized WebXR tool for the same workshop: put on a Quest 3 and see a CAD model standing on the real floor at 1:1. Raw WebXR device API with hit-test placement, a DOM-overlay HUD, and glTF's meters-as-units convention doing the scale work. About 650 lines of my own code plus a vendored three.js, served by a small Python script that generates its own TLS cert, since WebXR requires a secure context, and prints the LAN address for the headset. No internet, no build step, nothing installed on the headset.
