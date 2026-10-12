# ai-orchestra-web

**AI Orchestra** — a local-first workspace for several AI CLIs. The download page and the long-form documentation sit behind a password gate.

**https://hero-999-dev.github.io/ai-orchestra-web/**

## What is here

Behind the gate: `index.html`, the v0.1.0 download page, and `handover.html`, AI Orchestra Web. Open either file in a browser. The application source stays in the private `ai-orchestra` repository. No project markdown is published here.

## The gate

`index.html` asks for a password and derives `p-<sha256("orchestra:<password>")[:20]>/` in the browser. Neither the password nor the directory name is in the page source. A wrong password requests a directory that does not exist and gets a 404.

It locks the **link**, not the content. This repository is public, so anyone browsing the file list can see the directory. The gate keeps a URL from travelling further than it was handed.
