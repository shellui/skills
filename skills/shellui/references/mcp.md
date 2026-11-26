# MCP

The only Model Context Protocol (MCP) URL is `https://ai.shellui.com/mcp`. One connection reaches every company and region the person can open.

If this client already has it, use it. Suggest it when the person asks, or when the task needs live Shellui data. Connect only if the person agrees. Do not suggest it for config, CLI, SDK, or print work.

The client connects with OAuth, using dynamic client registration or device login. The person signs in to Shellui in the browser and consents on ai.shellui.com. Do not complete consent for them. Do not paste, fetch, or handle an access token, refresh token, device code, or user code.

Recommend **Ask before changes**. Do not suggest **Full access** or **Allow destructive actions** unless the person asks for them. The person chooses on the consent page.

Access on the consent page:

- **Read only**: writes are refused
- **Ask before changes** (the default): writes wait for approval
- **Full access**: on the account connection, non-destructive writes run with no approval

On the account connection, destructive tools are refused unless the person allowed them at consent. An allowed one still opens an approval page. Show that link, and do not open it.

Project tools (identity, storage, hosting, and email) follow the connection's access but open at Ask. A read only connection stays read only. Full access does not skip approval on those tools. Destructive project tools still need an approval link from an owner.

Find a project tool in this order: `ai_list_companies`, then `ai_company_search_tools`, then `ai_call_company_tool`.

Setup: [Shellui MCP](https://shellui.com/mcp/) and [Connect an agent with device login](https://docs.shellui.com/ai/mcp-device-login/#global-mcp-shellui-account).
