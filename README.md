# Jester Blog public site

Published site: https://eurus061.github.io/

This repository contains reviewed public static output in `site/` and the scheduled/manual Pages publishing workflow. Article sources and drafts stay in separate private repositories.

Use the **Publish blog** workflow in Actions to publish immediately. Otherwise it checks both the article and site source main branches for changes about every 15 minutes. GitHub schedules may be delayed.

The workflow uses standard public-repository Linux runners, without Codespaces, paid runners, npm cache or retained build artifacts.

Both private repositories follow their latest main revision. Commit article changes to the content repository or page/style changes to the source repository, then run the same workflow. No source commit number needs to be copied into the content repository. Each successful deployment records the exact pair of revisions.
