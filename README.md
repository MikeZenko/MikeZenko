# Hey World, I'm Tair

I'm a web developer, mostly TypeScript. I also founded [STEM Central Asia](https://stemac.vercel.app), a student-led organization that helps students in six Central Asian countries get into STEM. I like making complex things as simple as possible.

## What I've built

**[CarbonFlow](https://carbonflow.net)** ([repo](https://github.com/MikeZenko/carbonflow)). A live marketplace that matches carbon capture producers with industrial consumers. React on the front, Flask on the back. The matching is deliberately not an LLM: cosine similarity over engineered feature vectors, so you can see why a pair ranked where it did.

**[STEM Central Asia](https://stemac.vercel.app)** ([repo](https://github.com/MikeZenko/STEMAC)). The organization's website. React, TypeScript, Vite, Tailwind.

**[HBA Foundation scholarship platform](https://hbafg.vercel.app/scholarships)** ([repo](https://github.com/MikeZenko/HBA_Foundation)). A scholarship database for a foundation that helps students study abroad. Students submit scholarships they find, admins review them before they go live. Express and TypeScript backend, Next.js frontend. Deployed, though behind an access password: the foundation shares it privately with its students.

## What I'm working on now

This work is in private repos, so no links. Happy to walk through any of it.

**Amanuensis.** A Mac app for drafting prose that sounds like you, not like a model. It learns a persona from your writing samples, then drafts, critiques, and revises with a different model per pass. The part I care about most: the voice-match score is backed by a held-out eval, and every claim the app makes sits in a ledger with how it was measured. Drafts never leave your machine.

**Brodyaga.** A camera rover for a sculpture workshop, built with a small team. Eleven cameras, about 340 ArUco markers on the walls, ceiling projectors that show the sculptor where to work next. My part is accuracy: modeling detection noise, getting honest error bars out of the bundle adjustment, and fixing corner detection. Independent cameras currently agree on placement to about 2 cm. A calibration change only ships if it wins on held-out positions.

**Workshop AR viewer.** A weekend-sized WebXR tool for the same workshop: put on a Quest 3 and see a CAD model standing on the real floor at 1:1. Plain three.js, no build step, served off a tiny Python script on the shop LAN.

## Stack

TypeScript, React, Next.js, Node. Python with NumPy, SciPy, and OpenCV when the problem is vision or ML. I deploy on Vercel and Railway.
