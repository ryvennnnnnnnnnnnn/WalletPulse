# WalletPulse

**Know when your wallets move.**

WalletPulse is a Solana wallet monitoring tool that tracks on-chain activity and sends alerts directly to Discord.

## Download

Download the latest version from the [GitHub Releases](https://github.com/TradeLogDEV/WalletPulse/releases) page.

## Features

- **Real-time monitoring** — Monitor selected Solana wallets.
- **Buy and sell alerts** — Receive Discord notifications for detected trading activity.
- **Platform detection** — Recognizes activity across supported Solana platforms, including Pump.fun, PumpSwap, Raydium, Meteora, Orca, and Jupiter.
- **Discord management** — Add, remove, and organize wallets using slash commands.
- **Smart noise control** — Reduce duplicate and irrelevant alerts.
- **Recovery handling** — Recover from WebSocket disconnections and check for missed activity.
- **Latency diagnostics** — Inspect system status and alert performance.
- **Local data storage** — Keep wallet lists and settings on your machine.

## Requirements

- Windows
- Node.js 20 or newer
- Discord bot token and webhook
- Solana RPC access

## Getting Started

1. Download the latest release from [GitHub Releases](https://github.com/TradeLogDEV/WalletPulse/releases).
2. Extract the downloaded files.
3. Configure your Discord credentials and environment variables.
4. Run `DEV-LAUNCHER.bat`.
5. Use the Discord slash commands to add and monitor wallets.

## Discord Commands

WalletPulse supports commands for managing wallets, organizing groups, checking system status, and testing alerts.

Examples include:

- `/wallet add`
- `/wallet remove`
- `/wallet list`
- `/wallet info`
- `/group create`
- `/group list`
- `/status`
- `/latency`
- `/recent`
- `/test`

## Supported Activity

WalletPulse attempts to identify activity such as:

- Buys and sells
- Large buys and sells
- Token transfers
- New token activity
- Wallet convergence
- Other recognized or unknown transactions

Detection depends on available transaction data and supported on-chain programs.

## Optional PumpPortal Integration

WalletPulse can use the PumpPortal account-trade feed when a `PUMPPORTAL_API_KEY` is configured.

This integration is optional.

## Security

- Never share your Discord bot token, webhook URLs, RPC credentials, or API keys.
- Keep your local configuration and `walletpulse-data.json` private.
- Do not commit secrets or personal wallet data to GitHub.

## Troubleshooting

**Alerts are delayed or missing**
- Check your Solana RPC connection.
- Verify your Discord credentials and webhook.
- Check `/status` and `/latency`.
- Remember that public RPC endpoints can be unreliable.

**Wallet activity is not recognized**
- Some transactions may not be fully classified.
- Detection depends on the available transaction data and supported programs.

## Contributing

Bug reports, suggestions, and improvements are welcome. Please open an issue or submit a pull request through the repository.

## Creator

Created by [@ryvennnnnnnnnnnnn](https://github.com/ryvennnnnnnnnnnnn).

## Disclaimer

WalletPulse is a monitoring tool, not financial advice. Alerts may be delayed, incomplete, or incorrectly classified. Always verify transactions independently before making trading decisions.

**WalletPulse — Know when your wallets move.**
