# Setup and pre-publication checklist

## Before importing
- [ ] Download or clone the repository and review `workflow.json` before importing.
- [ ] Use a test n8n instance and keep the workflow inactive.
- [ ] Back up your n8n instance.
- [ ] Install only community nodes you trust and review their source.
- [ ] Install FFmpeg in the same runtime/container where n8n executes commands.
- [ ] Create a writable mounted directory and update every `/data/stories` path accordingly.

## Configure your own credentials and resources

This is a workflow template, not a bundle of the maintainer's accounts. Create credentials in your own n8n instance and select them in the nodes you choose to use.

- [ ] For OpenAI-based nodes, create and select your own OpenAI credential only if you choose to use that path; check current pricing before running.
- [ ] For Google Text-to-Speech, Sheets, Drive, or YouTube nodes, set up your own Google credentials and consent/OAuth flow as required.
- [ ] Configure any image-generation/community node required by the branch you enable; verify its current terms and any costs.
- [ ] Replace placeholder spreadsheet/tab/folder IDs with resources you own, or disable/remove those nodes.
- [ ] Never send your API keys, OAuth tokens, or exported credentials to the workflow maintainer or commit them to GitHub.

## Local-first mode and cost

The repository intends to support a local-first path plus optional integrations, but the current export has not yet been fully converted and tested for local-only operation. Until a tested local path is provided, treat the cloud integrations as optional but potentially chargeable. Before claiming a no-paid-API setup, replace those nodes with local tools, verify model/voice licenses, and run a complete end-to-end test without cloud API keys.

## Safety and testing
- [ ] Review all Execute Command nodes before running.
- [ ] Check all file paths and expected filenames; ensure directories exist.
- [ ] Check the workflow's connected branches and remove obsolete branches.
- [ ] Keep YouTube upload disabled until you have reviewed a test video.
- [ ] Confirm upload privacy, title, description, tags, and audience settings.
- [ ] Test with a single scene before processing a full batch.
- [ ] Verify a final MP4 plays correctly and has expected audio/video duration.

## Public GitHub repository
- [ ] Search the entire repository for API keys, OAuth tokens, emails, private URLs, webhook secrets, and account-specific IDs.
- [ ] Do not upload n8n credential exports, execution logs, private input data, or generated media without permission.
- [ ] Review the `LICENSE` and make sure you are comfortable allowing commercial reuse under MIT.
- [ ] Add screenshots/demo video only if you own the rights to publish them.
- [ ] Verify provider pricing, model/voice licenses, and terms; do not promise “100% free” unless every dependency and usage path has been checked.
- [ ] Configure `.github/FUNDING.yml` with your actual donation username only after creating that account/profile.
