# No-Cost AI Shorts Video Workflow

A community workflow template for experimenting with automated short-form video creation in n8n. The sanitized export includes story/quiz generation, image prompts/generation branches, narration, FFmpeg assembly, and optional Google Drive/YouTube integrations.

**Your own credentials stay yours.** This repository must never contain the maintainer's API keys, OAuth tokens, credential exports, or private account resources. Users import the template into their own n8n instance and configure their own credentials and resource IDs where needed.

> **Cost status:** This workflow is not yet a verified zero-cost, end-to-end local pipeline. The current export contains references to OpenAI and Google Cloud Text-to-Speech, and may use external image-generation services. Those services may have usage limits or charges. The intended direction is a local-first setup plus optional cloud integrations, but local replacements must be installed and tested before claiming that the complete workflow works without paid APIs.

## What's included

- `workflow.json` — sanitized export of the uploaded n8n workflow.
- `SETUP.md` — import, configuration, and security checklist.
- `.gitignore` — excludes common secrets, logs, and generated media.
- `.github/FUNDING.yml` — optional GitHub funding-button template; edit it only after creating a funding profile.
- `LICENSE` — MIT license for this project’s original material. See the licensing note below.

## Current status

This is a **sanitized, experimental export**, not a tested one-click product. The original workflow contains multiple legacy/alternative branches, local FFmpeg commands, community nodes, and integrations that need configuration. It has not been executed end-to-end in a clean environment.

## Requirements

- A self-hosted n8n instance. Several nodes execute shell commands and read/write local files; these are not suitable for every hosted n8n environment.
- FFmpeg installed in the same runtime/container where n8n executes commands.
- Any community nodes used by the branches you enable. Install only nodes you trust and review their source.
- Credentials for whichever optional integrations you enable. The current export includes cloud-service integrations; they are not guaranteed to be free.
- A writable working directory. The exported workflow uses `/data/stories` as a placeholder path; adjust it to a mounted writable directory in your deployment.

## Quick start

1. Download or clone this repository.
2. Import `workflow.json` into a **test** n8n instance.
3. Keep the workflow inactive while configuring it.
4. Open nodes that require credentials and select credentials you created in your own n8n instance. This export does not include the maintainer's credential secrets.
5. Replace the placeholder Google Sheets spreadsheet ID, sheet/tab ID, and Google Drive folder ID with resources you own—or disable/remove those integrations.
6. Confirm every local path in Read/Write Files and Execute Command nodes matches your environment.
7. Review and simplify the legacy/alternative branches before running. Do not assume every branch is connected or compatible.
8. Test with non-sensitive sample data and inspect each node's output. Review the final video manually before enabling publishing.

See [SETUP.md](SETUP.md) for the detailed checklist.

## Local-first + optional integrations roadmap

The project goal is to support two modes:

- **Local-first mode:** local models and self-hosted tools for generation and rendering, without requiring paid API keys.
- **Optional integrations:** users may configure their own cloud accounts and credentials if they choose.

The current exported workflow has **not yet been converted and tested** to provide a complete local-first path. Until that work is done, do not describe the current version as “100% free” or “no API keys required.” Local inference also uses hardware, disk space, and electricity, and model/voice licenses vary.

## Privacy and security

- Never commit API keys, OAuth tokens, exported credentials, personal spreadsheet IDs, private Drive folder IDs, private webhook URLs, execution logs, or sensitive input data.
- Shell execution nodes run commands with the permissions of your n8n process. Review all commands before enabling the workflow.
- YouTube publishing can post publicly. Disable or remove the upload node until you have tested the output and configured privacy settings.
- Users should create and select their own credentials in their own n8n instance. Never ask them to send credentials to the maintainer.
- Comply with provider terms, YouTube policies, copyright, model/voice licenses, and applicable disclosure rules.

## Support the project

This workflow is free to use. If it saves you time, consider making a voluntary donation to support maintenance, testing, documentation, and future improvements. Donations are optional and do not guarantee specific features or support response times.

See the repository’s **Sponsor** button if enabled. The `.github/FUNDING.yml` file is only a template; the maintainer must configure a real funding profile before a button can appear.

## License

This project’s original material is licensed under the MIT License; see [`LICENSE`](LICENSE). MIT permits reuse, modification, redistribution, and commercial use, provided the license and copyright notice are preserved. If you do **not** want others to sell or commercially reuse their own versions, do not publish with MIT; choose a noncommercial license instead, understanding that it would not be an OSI-approved open-source license.

This license does not grant rights to third-party software, n8n, community nodes, model weights, voices, images, or other assets. Their own terms apply. n8n uses its own Sustainable Use License / other licensing terms; review [n8n's official license guidance](https://docs.n8n.io/sustainable-use-license/) before redistributing or offering a hosted service based on n8n.

## Roadmap

- Consolidate the supported path and remove obsolete branches.
- Implement and test a local-first generation path.
- Keep optional cloud integrations clearly separated from the local path.
- Add error handling, retries, and provider rate-limit handling.
- Make output directory and provider/model choices configurable.
- Add a dry-run mode and default YouTube uploads to private/unlisted.
- Document a verified end-to-end test matrix.

## Disclaimer

This project is provided as-is, without warranty. Provider pricing, APIs, node compatibility, model licenses, and platform policies can change.
