# Cross-Platform Deployment Matrix

Verified against official vendor documentation on 2026-07-23. Recheck capabilities, plan requirements, and URLs immediately before deployment.

The detailed human setup guide is maintained in the Notion project:

- [dAItrader — Cross-Platform Deployment Guide](https://app.notion.com/p/3a68b48d557981f5a7aafd27a03916ef)

## Shared contract

Every platform must preserve:

- exact model and prompt version;
- contender ID and isolation key;
- assigned cohort and information cutoff;
- one independent decision cycle;
- the same structured output contract;
- no access to competitor outputs;
- referee-controlled fictional execution and scoring.

## Capability matrix

| Platform | Persistent configuration | Native recurring execution | Notion access | Recommended deployment |
|---|---|---:|---:|---|
| Notion | Custom Agents | Yes | Native | Contender Custom Agent plus separate Referee Agent |
| ChatGPT | Projects or custom GPTs | Scheduled Tasks | Connected app | Scheduled Task reading/writing authorized Notion records |
| Claude | Projects | No verified native Project scheduler | Connector | Claude Project for manual use; Claude Code/API via n8n or cron for recurring runs |
| Gemini | Gems or Spark skills | Scheduled Actions or Spark schedules | External integration may be required for controlled writes | Gem for configuration; Spark/API workflow for recurring runs |
| Grok | Skills | Automations | Catalog connector | Skill plus Automation plus Notion connector |
| Microsoft Copilot | Agent Builder or Copilot Studio | Copilot Studio flows or Copilot Tasks | Custom connector generally required | Copilot Studio agent with scheduled agent flow |
| API or local model | Repository prompt files | External scheduler | Notion API or n8n | n8n-controlled structured run with referee validation |

## Official references

### Notion

- https://www.notion.com/help/custom-agents

### OpenAI / ChatGPT

- https://help.openai.com/en/articles/10169521-projects-in-chatgpt
- https://help.openai.com/en/articles/8554407-gpts-in-chatgpt
- https://help.openai.com/en/articles/10291617-tasks-in-chatgpt

### Anthropic / Claude

- https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects
- https://support.anthropic.com/en/articles/11817150-connect-your-tools-to-unlock-a-smarter-more-capable-ai-companion
- https://docs.anthropic.com/en/docs/claude-code/cli-usage

### Google / Gemini

- https://support.google.com/gemini/answer/15235603
- https://support.google.com/gemini/answer/16316416
- https://support.google.com/gemini/answer/17094710

### xAI / Grok

- https://x.ai/news/grok-skills
- https://x.ai/news/grok-automations
- https://docs.x.ai/grok/connectors

### Microsoft Copilot

- https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/flows-overview
- https://support.microsoft.com/en-US/microsoft-copilot/using-copilot-tasks

## Deployment test

Before enabling a recurring schedule:

1. Register the exact model and platform in Notion.
2. Run one historical dry test.
3. Confirm the output validates against `schemas/daitrader-records.schema.json`.
4. Confirm the contender can access only its own operational state.
5. Confirm no real financial action is possible.
6. Confirm the referee can reproduce fictional fills, costs, and snapshot totals.
7. Mark all dry-test data and exclude it from official scoring.
