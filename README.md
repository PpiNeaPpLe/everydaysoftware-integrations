# Everyday Software Voice Demo

Prepare a link to try an AI receptionist using a public business homepage.

**Endpoint:** `https://everydaysoftware.ai/mcp/voice-demo`  
**Transport:** MCP Streamable HTTP  
**Authentication:** none  
**Tool:** `prepare_voice_demo_link({"website_url":"https://yourbusiness.com"})`

The tool returns a link with the website prefilled. Open it, select **Build My
Demo**, then **Start Talking** and allow your microphone. The browser demo lasts
up to five minutes. The tool itself does not fetch websites or start paid voice
sessions. It creates no phone number or production agent.

The demo is independent of the source business. It reads its public homepage;
no sign-in pages, account credentials, or private systems are needed. It cannot
book appointments or dispatch staff. Everyday Software reviews conversations,
and any messages taken in a demo go to the Everyday Software demo team.

## Connect

In a client that supports remote MCP, add the endpoint with Streamable HTTP and
no authentication. A generic configuration is:

```json
{
  "mcpServers": {
    "everydaysoftware-voice-demo": {
      "type": "streamable-http",
      "url": "https://everydaysoftware.ai/mcp/voice-demo"
    }
  }
}
```

For ChatGPT, open [Plugins](https://chatgpt.com/plugins), select the plus button
and **Add custom MCP server**, then enter the endpoint and choose no
authentication. Availability depends on your account and workspace policies.
This is a manual connection, not evidence of a directory listing.

For Gemini CLI, install this extension and restart Gemini CLI:

```sh
gemini extensions install https://github.com/PpiNeaPpLe/everydaysoftware-integrations
```

Then ask: "Prepare a voice-demo link for https://everydaysoftware.ai."
The extension uses the same public endpoint and requires no API key. See the
[Gemini CLI extension guide](https://geminicli.com/docs/extensions/) for installation details.

The `openai/` folder contains a portable plugin package. `server.json` contains
MCP Registry metadata; `gemini-extension.json` contains the Gemini CLI extension.
Version 0.1.0 is published in the
[official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers/io.github.PpiNeaPpLe%2Feverydaysoftware-voice-demo/versions/0.1.0).
This registry entry is separate from approval or listing in ChatGPT or other
client directories.

[Try the demo](https://everydaysoftware.ai/demo-my-website) ·
[Privacy](https://everydaysoftware.ai/privacy-policy) ·
[Terms](https://everydaysoftware.ai/terms)
