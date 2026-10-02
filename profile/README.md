<p align="center">
  <a href="https://lastping.dev">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/hero-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/hero-light.svg">
      <img alt="LastPing. A stopped agent looks exactly like a thinking one. Monitoring for AI agent runs, cron jobs and CI/CD. Free for individuals." src="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/hero-light.svg" width="100%">
    </picture>
  </a>
</p>

<p align="center">
  <a href="https://lastping.dev"><img alt="Website" src="https://img.shields.io/badge/Website-0f766e?style=for-the-badge"></a>
  <a href="https://app.lastping.dev/docs"><img alt="API docs" src="https://img.shields.io/badge/API%20docs-2f3a49?style=for-the-badge"></a>
  <a href="https://lastping.dev/mcp/"><img alt="MCP server" src="https://img.shields.io/badge/MCP%20server-2f3a49?style=for-the-badge"></a>
  <a href="https://lastping.dev/terraform"><img alt="Terraform" src="https://img.shields.io/badge/Terraform-2f3a49?style=for-the-badge"></a>
  <a href="https://app.lastping.dev/status/lastping-self"><img alt="Status" src="https://img.shields.io/badge/Status-2f3a49?style=for-the-badge"></a>
  <a href="https://lastping.dev/changelog"><img alt="Changelog" src="https://img.shields.io/badge/Changelog-2f3a49?style=for-the-badge"></a>
</p>

<p align="center">
  LastPing waits for your jobs to check in. When an expected signal never arrives, it opens an incident and tells you.<br>
  <b>Free for individuals.</b> No credit card required.
</p>

<br>

<h3 align="center">What LastPing watches</h3>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/features-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/features-light.svg">
    <img alt="Cron and heartbeats: your job curls one URL when it finishes; miss the window, get an incident. CI/CD: one signed webhook from GitHub Actions, GitLab CI or Jenkins catches runs that fail, hang or never start. HTTP uptime: status code, latency and keyword checks on a schedule. AI agent runs: started, progress, blocked, failed; a run that stops making progress is caught at the step it stalled on. Tracing: spans, tokens and estimated cost for traced agent runs, sent over OpenTelemetry. 9 alert destinations: email, Slack, Discord, Telegram, ntfy, Pushover, Microsoft Teams, Google Chat and a signed webhook." src="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/features-light.svg" width="100%">
  </picture>
</p>

<p align="center">
  Alerts are routed per monitor and event. One incident, not a storm, and it closes by itself when the job checks back in.
</p>

<details>
<summary>The same list as text</summary>

| Signal | How it works |
|---|---|
| **Cron and heartbeats** | Your job curls one URL when it finishes. Miss the window, get an incident. |
| **CI/CD** | One signed webhook from GitHub Actions, GitLab CI or Jenkins, no YAML changes. Catches runs that fail, hang or never start. |
| **HTTP uptime** | Status code, latency and keyword checks on a schedule. |
| **AI agent runs** | Started, progress, blocked, failed: a run says where it is, and a long run that stops making progress is caught at the step it stalled on. |
| **Tracing** | Traced agent runs show spans, tokens and estimated cost, sent over OpenTelemetry. |
| **Alerts** | 9 destinations: email, Slack, Discord, Telegram, ntfy, Pushover, Microsoft Teams, Google Chat and a signed webhook. |

</details>

<br>

<h3 align="center">From a failed run to a note the next run reads</h3>

<p align="center">
  <a href="https://lastping.dev">
    <img alt="An agent run goes from running to failed, LastPing opens an incident and delivers the alert, and the next run reads the open incident over MCP and adds a note to it." src="https://raw.githubusercontent.com/lastping-dev/.github/main/profile/assets/demo-loop.webp" width="100%">
  </a>
  <br>
  <sub>A demo with sample data.</sub>
</p>

<br>

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

[lastping.dev](https://lastping.dev) &nbsp;&middot;&nbsp; [API reference](https://app.lastping.dev/docs) &nbsp;&middot;&nbsp; [MCP server](https://lastping.dev/mcp/) &nbsp;&middot;&nbsp; [Terraform](https://lastping.dev/terraform) and the [Terraform Registry](https://registry.terraform.io/providers/lastping-dev/lastping) &nbsp;&middot;&nbsp; [Status](https://app.lastping.dev/status/lastping-self) &nbsp;&middot;&nbsp; [Changelog](https://lastping.dev/changelog) &nbsp;&middot;&nbsp; [hello@lastping.dev](mailto:hello@lastping.dev)

<br>

<p align="center">
  <a href="https://app.lastping.dev"><img alt="Start monitoring free" src="https://img.shields.io/badge/Start%20monitoring%20free-0f766e?style=for-the-badge"></a>
</p>
