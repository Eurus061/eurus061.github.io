# Jester Blog public releases

Official site: [blog.365hbgj.com](https://blog.365hbgj.com/)
Backup site: [eurus061.github.io](https://eurus061.github.io/)

This repository contains reviewed public static output in `site/`, two publishing workflows, and separate successful publication records. Article sources, drafts, deployment configuration and backups remain private.

Use **Publish production blog** in Actions to publish the official domain immediately. It reads the latest main revisions of the private content and source repositories, checks and builds them, uploads a constrained static release through a dedicated SSH key, and records `.production.json` only after origin HTTPS checks pass. Otherwise it checks about every 15 minutes; GitHub schedules may be delayed.

**Publish blog** independently updates the backup GitHub Pages site and `.publication.json`. Both builds use the official domain for canonical URLs, RSS and sitemap. Pages success does not imply that the production upload succeeded.

Standard public-repository Linux runners are used, without Codespaces, paid runners, npm cache or retained build artifacts. No source commit needs to be copied into the content repository. A failed production activation restores the previous static release; the initial WordPress files and database are kept for administrator recovery.
