# Autogen Blog

Automatically generate data/tech posts, open a PR for review, and publish to Hashnode only after merge.

- `scripts/generate_post.py` → creates a Markdown draft post
- `.github/workflows/generate-and-pr-open.yml` → scheduled + manual trigger that runs the script and opens a PR
- `.github/workflows/publish-to-hashnode.yml` → on merge to main, posts to Hashnode via API

## Setup

1. Add GitHub secrets:
   - `HASHNODE_API_KEY` – your Hashnode API token
   - `AUTHOR_NAME` (optional)
2. Edit the cron schedule, tags, or template inside the Python script as you like.
