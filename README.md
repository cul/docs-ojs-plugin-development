# Developer Docs for OJS3 Plugins

## Capistrano Tasks for CUL deploys
The CUL Capistrano deploy tasks are defined in cul/ds-ojs

## Capistrano Deploy Patterns
1. fetch the OJS distribution TAR file
2. unpack into deployment root, remove TAR
3. set up robots.txt
4. symlink log files
5. copy themes from ds-ojs repository

### Open Questions
- Better to develop themes in ds-ojs, or separately and use subrepos (lke OJS distro does)
- Similarly, how to deploy plugins generally (and configure relevant plugins for an install)
- Tracking the OJS config file (either via mechanisms to track YAML configs in other apps or under version control)

## URL Patterns
See also [URL notes](URLS.md)

---
See also [Background notes](BACKGROUND.md)