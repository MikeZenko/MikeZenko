# Hi, I'm Tair

I'm a web developer working mostly in TypeScript, and the founder of [STEM Central Asia](https://stemac.vercel.app), a student-led organization connecting students across six Central Asian countries with STEM opportunities. I like building complex things as simply as possible.

## What I've built

**[CarbonFlow](https://carbonflow.net)** ([repo](https://github.com/MikeZenko/carbonflow)). A marketplace that matches carbon capture technology producers with industrial consumers. React frontend, Flask backend, vector-based match scoring with NumPy and scikit-learn, JWT auth. Deployed and live.

[![CarbonFlow landing page](assets/carbonflow.png)](https://carbonflow.net)

**[STEM Central Asia](https://stemac.vercel.app)** ([repo](https://github.com/MikeZenko/STEMAC)). The organization's website: React, TypeScript, Vite, Tailwind.

**[HBA Foundation scholarship platform](https://github.com/MikeZenko/HBA_Foundation)**. A scholarship database built for a foundation that helps students find educational opportunities abroad. Express and TypeScript backend, Next.js frontend, with an admin workflow for reviewing community submissions.

## What I'm working on now

These live in private repos, so no links, but I'm happy to walk through any of them.

**Amanuensis.** A local Mac app for drafting prose in your own voice. An Electron and React frontend drives a Python sidecar that builds personas from your writing samples, routes each pass (draft, critique, revise) to a different model, and scores every take with a stylometric voice gauge that is validated on held-out passages rather than asserted. The eval suite implements the Fast-DetectGPT detector locally and audits it against the RAID benchmark, and every user-facing claim is tracked in a ledger with its measurement status. Drafts never leave the machine.

**Brodyaga.** A measuring and projection system for a sculpture workshop, built with a small team. A rover with an 11-camera rig localizes itself against a photogrammetric map of about 340 ArUco markers, and ceiling projectors guide the sculptor's next action. I work on the accuracy layer: a fitted observation-noise model that weights each detection by apparent marker size, posterior covariance computed from the bundle adjustment's robust Gauss-Newton Hessian, and corner-detection fixes (AprilTag refinement gated by cross-detector agreement, burst merging while the rover is stationary). Rig placement consensus is currently around 2 cm at 1.6 px reprojection error, and calibration changes are accepted or rejected on held-out positions.

**Workshop AR viewer.** A dependency-free WebXR prototype that places CAD models at true 1:1 scale in the same workshop through Quest 3 passthrough. three.js with raw WebXR hit-testing and a self-hosted Python launcher, so it runs on the shop LAN with no internet and no headset app install.

## Stack

TypeScript, React, Next.js, Node and Express on the web side. Python with NumPy, SciPy, and OpenCV for computer vision, and Flask and scikit-learn when a project needs ML. I deploy on Vercel and Railway.
