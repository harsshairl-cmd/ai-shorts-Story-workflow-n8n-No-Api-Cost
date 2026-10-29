# ai-shorts-Story-workflow-n8n-No-Api-Cost
Create AI-powered YouTube Shorts with n8n 🚀 Automate story &amp; quiz generation, image prompts, narration, and FFmpeg video assembly. Open-source workflow template with optional Google Drive/YouTube integrations and a local-first roadmap. Experimental—setup.
# 🎬 AI Shorts Workflow — n8n Automation

**Build AI-powered short-form videos with an open-source n8n workflow.**

Turn your ideas into short-form video experiments using story and quiz generation, image prompts, narration, and FFmpeg-based video assembly.

The goal is to make AI video creation workflows easier to explore, customize, and improve—with a long-term focus on local-first tools and optional cloud integrations.

[Explore the Workflow](workflow.json) · [Setup Guide](SETUP.md) · [Support the Project](#-support-the-project)

## ✨ What You Can Explore

- 🧠 **Story & Quiz Generation** — experiment with automated short-form content ideas.
- 🎨 **Image Generation Branches** — create image prompts and connect supported image-generation services.
- 🎙️ **Automated Narration** — configure text-to-speech integrations.
- 🎞️ **Video Assembly** — use FFmpeg to combine media into video output.
- ☁️ **Optional Cloud Integrations** — configure your own Google Drive and YouTube integrations.
- 🏡 **Local-First Roadmap** — work toward a setup that reduces dependence on paid APIs.

## ⚠️ Project Status

This is an experimental, sanitized workflow export—not a verified one-click solution.

The current workflow references cloud services and may incur costs. Some branches, community nodes, credentials, and local paths require configuration and testing.

**A complete, verified zero-cost local pipeline is a future goal, not a current guarantee.**

## 🚀 Get Started

1. Clone or download this repository.
2. Import `workflow.json` into a test instance of n8n.
3. Follow [SETUP.md](SETUP.md) to configure your environment.
4. Install and review the required nodes and FFmpeg.
5. Configure your own credentials and resource IDs.
6. Test each enabled branch using non-sensitive sample data.
7. Review generated videos before publishing.

## 🔒 Security First

Never commit API keys, OAuth tokens, exported credentials, private resource IDs, or sensitive execution logs. Review shell-execution nodes before running the workflow, and test YouTube uploads with private or unlisted visibility first.

Use your own n8n credentials and accounts. Never share secrets with the maintainer.

## 🗺️ Roadmap

- [ ] Simplify and document the supported workflow.
- [ ] Implement and test a local-first generation path.
- [ ] Separate optional cloud integrations from local processing.
- [ ] Improve error handling and retry behavior.
- [ ] Add configurable models, providers, and output paths.
- [ ] Document end-to-end testing results.

## ❤️ Support the Project

If this workflow saves you time or helps you learn, consider supporting its continued development.

Your voluntary support can help with testing, documentation, maintenance, and future improvements.

Donations are optional and do not guarantee specific features or response times.

## 📜 License

The project's original material is intended to be released under the MIT License. Third-party software, n8n, community nodes, models, voices, and other assets remain subject to their own licensing terms. Review the included `LICENSE` and the relevant third-party terms before redistribution.

---

⭐ If you find this project useful, star the repository, share it with other creators, or contribute an improvement.
