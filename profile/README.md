<p align="center">
  <a href="https://lastping.dev">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/logo-dark.png">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/logo-light.png">
      <img alt="LastPing" src="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/logo-light.png" width="260">
    </picture>
  </a>
</p>

<h3 align="center">Monitoring for AI agent runs, cron jobs and CI/CD.</h3>

<p align="center">
  LastPing waits for your jobs to check in. When an expected signal never arrives, it opens an incident and tells you.<br>
  <b>Free for individuals.</b> No credit card required.
</p>

<p align="center">
  <a href="https://lastping.dev"><b>Website</b></a> &nbsp;&middot;&nbsp;
  <a href="https://app.lastping.dev/docs">API docs</a> &nbsp;&middot;&nbsp;
  <a href="https://lastping.dev/mcp/">MCP server</a> &nbsp;&middot;&nbsp;
  <a href="https://lastping.dev/terraform">Terraform</a> &nbsp;&middot;&nbsp;
  <a href="https://app.lastping.dev/status/lastping-self">Status</a> &nbsp;&middot;&nbsp;
  <a href="https://lastping.dev/changelog">Changelog</a>
</p>

---

### What LastPing watches

| Signal | How it works |
|---|---|
| **Cron and heartbeats** | Your job curls one URL when it finishes. Miss the window, get an incident. |
| **CI/CD** | One signed webhook from GitHub Actions, GitLab CI or Jenkins, no YAML changes. Catches runs that fail, hang or never start. |
| **HTTP uptime** | Status code, latency and keyword checks on a schedule. |
| **AI agent runs** | Started, progress, blocked, failed: a run says where it is, and a long run that stops making progress is caught at the step it stalled on. |
| **Tracing** | Traced agent runs show spans, tokens and estimated cost, sent over OpenTelemetry. |

Alerts go to **9 destinations**: email, Slack, Discord, Telegram, ntfy, Pushover, Microsoft Teams, Google Chat and a signed webhook, routed per monitor and event. One incident, not a storm, and it closes by itself when the job checks back in.

### Quick start

**1. Ping from anything that can make an HTTP request.** Create a monitor at [app.lastping.dev](https://app.lastping.dev), then add one line to the end of your job:

```bash
curl -fsS -m 10 --retry 3 https://ping.lastping.dev/<id>
```

**2. Or let your AI assistant set it up.** Add the hosted MCP server to Claude, ChatGPT, Claude Code, VS Code, Codex or Gemini CLI and sign in. It gets 50 tools to create monitors, wire the ping, route alerts and read incidents.

```text
https://mcp.lastping.dev/mcp
```

**3. Or keep it in code with Terraform.** The official provider is on the public Terraform Registry.

```hcl
terraform {
  required_providers {
    lastping = {
      source  = "lastping-dev/lastping"
      version = "~> 0.5"
    }
  }
}
```

### Public repositories

| Repository | What it is | Release |
|---|---|---|
| [**terraform-provider-lastping**](https://github.com/lastping-dev/terraform-provider-lastping) | The official Terraform provider: monitors, destinations, routing and alert templates as code, plus export and import of what you already have. | [![Release](https://img.shields.io/github/v/release/lastping-dev/terraform-provider-lastping?label=registry&color=2dd4bf)](https://registry.terraform.io/providers/lastping-dev/lastping) [![License](https://img.shields.io/github/license/lastping-dev/terraform-provider-lastping)](https://github.com/lastping-dev/terraform-provider-lastping/blob/main/LICENSE) |
| [**lastping-app**](https://github.com/tp322d/lastping-app) | The open-source pieces: the `lastping` CLI and the MCP server, for the hosted service at lastping.dev. | [![Release](https://img.shields.io/github/v/release/tp322d/lastping-app?color=2dd4bf)](https://github.com/tp322d/lastping-app/releases) [![License](https://img.shields.io/github/license/tp322d/lastping-app)](https://github.com/tp322d/lastping-app/blob/main/LICENSE) |

### LastPing runs on LastPing

Its own ping ingest, API, remote MCP server and login page are watched on a [public status page](https://app.lastping.dev/status/lastping-self) anyone can open. Incidents stay visible.

### Links

- Website: [lastping.dev](https://lastping.dev)
- API reference: [app.lastping.dev/docs](https://app.lastping.dev/docs)
- MCP server: [lastping.dev/mcp](https://lastping.dev/mcp/)
- Terraform: [lastping.dev/terraform](https://lastping.dev/terraform) and the [Terraform Registry](https://registry.terraform.io/providers/lastping-dev/lastping)
- Status: [app.lastping.dev/status/lastping-self](https://app.lastping.dev/status/lastping-self)
- Changelog: [lastping.dev/changelog](https://lastping.dev/changelog)
- Contact: [hello@lastping.dev](mailto:hello@lastping.dev)

<p align="center"><a href="https://app.lastping.dev"><b>Start monitoring free</b></a></p>
