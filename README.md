# WalletPulse

### Know when your wallets move.

Real-time Solana wallet monitoring with Discord alerts.

WalletPulse lets you monitor selected Solana wallets, detect on-chain activity, and receive notifications directly in Discord. Manage watched wallets through Discord slash commands and review detected transactions with available token details and transaction links.

## Features

- **Real-time monitoring** — listen for activity from selected Solana wallets.
- **BUY & SELL alerts** — receive notifications for detected buy and sell activity.
- **Large trade alerts** — identify large buys and sells based on configured thresholds.
- **Transfer monitoring** — detect supported SOL and token transfers.
- **Token information** — include available token names, addresses, amounts, and links.
- **Platform detection** — recognize supported Solana platforms and programs, including Pump.fun, PumpSwap, Raydium, Meteora, Orca, and Jupiter.
- **Discord integration** — manage wallets and groups using slash commands.
- **Activity classification** — identify supported swaps, liquidity actions, token minting and burning, staking, claims, and other transaction activity when sufficient evidence is available.
- **Duplicate suppression** — reduce repeated notifications and unnecessary noise.
- **Reconnect recovery** — attempt to recover missed activity after listener interruptions.
- **Latency diagnostics** — inspect RPC, processing, and Discord delivery timings.
- **Optional PumpPortal integration** — use an additional wallet-specific BUY/SELL signal feed when configured.

## How It Works

1. WalletPulse monitors selected Solana wallets.
2. Detected transactions are retrieved and analyzed.
3. WalletPulse classifies the available transaction activity.
4. Relevant events are formatted into alerts.
5. Alerts are delivered to your configured Discord channel.

## Requirements

- Windows for the included launcher workflow.
- [Node.js](https://nodejs.org/) 20 LTS or newer recommended.
- A Discord server.
- A Discord bot and bot token.
- A Discord webhook for alert delivery.

## Getting Started

### 1. Download WalletPulse

Download the latest release from the GitHub Releases section and extract the ZIP archive.

### 2. Configure Discord

Create a Discord webhook in the channel where you want to receive alerts.

Then create a Discord application and bot through the [Discord Developer Portal](https://discord.com/developers/applications).

Invite the bot to your server with the `bot` and `applications.commands` OAuth scopes.

Keep your bot token and webhook URL private.

### 3. Launch

Run `DEV-LAUNCHER.bat` and follow the setup prompts to configure your Discord credentials.

The launcher handles the required dependency setup when needed.

WalletPulse runs in the terminal and uses Discord for wallet management. It does not require a browser dashboard.

### 4. Add a Wallet

Use the following slash command in your Discord server:

`/wallet add`

Provide the Solana wallet address and a name to identify it. You can optionally assign the wallet to a group.

Use `/status` to check the listener and `/test` to test the alert delivery pipeline.

## Discord Commands

| Command | Description |
|---|---|
| `/wallet add` | Add a wallet to monitor |
| `/wallet remove` | Remove a monitored wallet |
| `/wallet list` | List monitored wallets |
| `/wallet info` | View wallet details |
| `/group create` | Create a wallet group |
| `/group list` | List wallet groups |
| `/group add` | Add a wallet to a group |
| `/group remove` | Remove a wallet from a group |
| `/status` | View listener and system status |
| `/wallets` | View wallets and subscription status |
| `/recent` | View recent detected activity |
| `/latency` | View measured latency metrics |
| `/rpc` | View RPC configuration and health |
| `/test` | Send a test alert |

## Supported Activity

WalletPulse can detect and report supported activity types, including:

- `BUY`
- `SELL`
- `LARGE_BUY`
- `LARGE_SELL`
- `TRANSFER`
- `NEW_TOKEN`
- `CONVERGENCE`
- `UNKNOWN`

Additional activity may be identified depending on transaction data and available metadata.

Classification is best-effort. Some transactions may not contain enough information for reliable identification.

## Optional PumpPortal Integration

WalletPulse supports an optional PumpPortal account-trade feed for additional wallet-specific BUY/SELL signals.

This integration requires a `PUMPPORTAL_API_KEY` and may involve metered usage. Review PumpPortal's current documentation and pricing before enabling it.

WalletPulse can operate without this optional integration.

## Security

- Never publish Discord bot tokens, webhook URLs, or API keys.
- Do not commit `walletpulse-data.json` or other local configuration files.
- Remove credentials and private configuration from logs before sharing them.
- Rotate any credentials that are accidentally exposed.
- Review the code and dependencies before running the software.

## Troubleshooting

**Discord commands are missing**

Check that the bot is online, was invited with the `applications.commands` scope, and is running with a valid token.

**No alerts arrive**

Verify your webhook URL, Discord permissions, listener status, and monitored wallet configuration. Use `/test` to test Discord delivery.

**The listener disconnects**

Inspect the terminal output and `/rpc` command. Public RPC providers may rate-limit requests or experience interruptions.

**Token information is missing**

Token metadata depends on available upstream data and may not always be available.

## Contributing

Contributions, bug reports, documentation improvements, and feature suggestions are welcome.

When reporting a bug, include the WalletPulse version, operating system, steps to reproduce the issue, and relevant sanitized logs.

Never include API keys, Discord tokens, webhook URLs, or private configuration in public issues.

## Creator

Created by **ryvennnnnnnnnnnnn https://github.com/ryvennnnnnnnnnnnn**.

If you use or modify WalletPulse, please retain the original copyright and license notices and credit the project where practical.

## Disclaimer

WalletPulse is a wallet-monitoring and notification tool. It does not execute trades, custody funds, or guarantee the accuracy or profitability of detected activity.

Alerts may be delayed, incomplete, duplicated, or incorrectly classified. This software is provided for informational purposes only and does not constitute financial or investment advice.

Always perform your own research before making financial decisions.

---

**WalletPulse — Know when your wallets move.**
