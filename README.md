# DeepUptime plugins for Claude Code

The official [DeepUptime](https://deepuptime.com) plugin for Claude Code: uptime monitoring and on-call workflows through the DeepUptime MCP server.

## Install

In Claude Code:

```
/plugin marketplace add deepuptime/claude-plugins
/plugin install deepuptime@deepuptime
```

## Connect

Installing the plugin also adds the DeepUptime MCP server (`https://api.deepuptime.com/public/mcp`). Run `/mcp`, select the DeepUptime server and choose **Authenticate** to sign in with your DeepUptime account.

Prefer an API token? Create one under **Organization → API tokens** in the dashboard and add the server yourself:

```
claude mcp add --transport http DeepUptime https://api.deepuptime.com/public/mcp --header "Authorization: Bearer YOUR_API_TOKEN"
```

With a read-only token the server lists only the read tools.

## Skills

| Skill | What it does |
|---|---|
| `deepuptime-monitoring` | Create monitors, suggest what to watch after a deploy, pause or resume checks, schedule maintenance windows, model monitor dependencies, and take incidents through to the postmortem. |
| `deepuptime-on-call` | Find who is on call; acknowledge, snooze, resolve or escalate active pages; cover or swap a shift; and look into escalation runs and policies. |

The skills ask before anything that changes who gets paged or what is monitored. Read tools work on every plan, including Free; write tools require Pro or higher.
