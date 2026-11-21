# LinkBunny Exchange for Kiro

Run contextual nofollow link exchanges for sites you control. Use Kiro to review site status, prepare a site profile and work through link requests one at a time. The first exchange is free for one site. Paid plans cover more. [Plans and limits](https://getlinkbunny.com/pricing)

## Sign in

Use Node.js 22 or newer and a LinkBunny account. Browser sign-in uses macOS Keychain or a running Linux Secret Service. Run this in a terminal on the same machine and as the same user running Kiro.

```sh
npx -y @linkbunny/mcp@0.1.11 login
```

Complete sign-in in your browser. Kiro needs `npx` on its PATH and access to the local sign-in used by the package. On Windows or without a supported credential store, use the standalone configuration below and add the `--token-file` argument and an absolute path as described in the [private token-file setup](https://getlinkbunny.com/mcp#exchange).

## Install

Choose one Kiro setup for this server in a workspace.

- **Power.** Open Powers → Add Custom Power → Import power from a repository URL. Use `https://github.com/hboon/linkbunny-exchange-kiro`. The Power adds exchange guidance and the MCP connection.
- **Standalone MCP.** Use the button below and review the configuration Kiro shows.

[![Add to Kiro](https://kiro.dev/images/add-to-kiro.svg)](https://kiro.dev/launch/mcp/add?name=linkbunny-exchange&config=%7B%22command%22%3A%22npx%22%2C%22args%22%3A%5B%22-y%22%2C%22%40linkbunny%2Fmcp%400.1.11%22%5D%2C%22disabled%22%3Afalse%2C%22autoApprove%22%3A%5B%5D%7D)

To add the server manually, merge this into the workspace's `.kiro/settings/mcp.json`. Keep tool auto-approval empty.

```json
{
  "mcpServers": {
    "linkbunny-exchange": {
      "command": "npx",
      "args": ["-y", "@linkbunny/mcp@0.1.11"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Run **"Use LinkBunny Exchange to call get_status once and pause."** This checks your connection without reserving an assignment. Approve marketplace actions one at a time, including check-in, which can reserve an assignment. [Exchange workflow](https://getlinkbunny.com/skill.md)

## Privacy, support and license

The pinned [npm package](https://www.npmjs.com/package/@linkbunny/mcp/v/0.1.11) runs locally and sends account and exchange requests to the LinkBunny API over HTTPS. Keep keys in local sign-in storage or a private token file. [Privacy](https://getlinkbunny.com/privacy) · [Terms](https://getlinkbunny.com/terms) · [Support](https://getlinkbunny.com/about)

The files in this repository are [MIT licensed](LICENSE). The hosted service uses the linked LinkBunny terms.
