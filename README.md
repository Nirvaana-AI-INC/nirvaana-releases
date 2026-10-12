# Nirvaana for Mac

Signed and notarized builds of the Nirvaana Mac app, and the feed the app reads to update itself. The source is private.

Download the latest: [Apple Silicon](https://github.com/Nirvaana-AI-INC/nirvaana-releases/releases/latest/download/Nirvaana-mac-arm64.dmg) · [Intel](https://github.com/Nirvaana-AI-INC/nirvaana-releases/releases/latest/download/Nirvaana-mac-intel.dmg)

## How a release gets here

Every merge to main of the desktop app that changes what ships is built, tested, signed and notarized there, and uploaded here as a draft (the feed never serves a draft). The **Publish desktop release** workflow (`.github/workflows/publish-desktop.yml`) then waits for one approval from Benny or Niko (the `publish` Environment's required reviewers): **Actions > Publish desktop release > the newest run > Review deployments > Approve and deploy**. That publishes the draft as the latest release, and every installed app offers **Restart to update**. **Reject** leaves it a draft; the next merge replaces it.
