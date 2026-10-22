# WalletPulse

**Know when your wallets move.**

WalletPulse is a Solana wallet monitoring tool that tracks on-chain activity and sends alerts directly to Discord.

## Download

Download the latest version from the [GitHub Releases](https://github.com/ryvennnnnnnnnnnnn/WalletPulse/releases) page.

## Features

- Real-time Solana wallet monitoring
- Buy and sell alerts
- Token and platform detection
- Discord slash commands for wallet management
- Wallet groups
- Activity history and status monitoring
- Alert latency diagnostics
- WebSocket reconnection and recovery
- Local storage for wallet data and settings

## Requirements

- Windows
- Node.js 20 or newer
- Discord bot token and webhook
- Solana RPC access

## Getting Started

1. Download the latest release from [GitHub Releases](https://github.com/ryvennnnnnnnnnnnn/WalletPulse/releases).
2. Extract the downloaded ZIP.
3. Configure the required credentials and environment variables.
4. Run `DEV-LAUNCHER.bat`.
5. Use Discord slash commands to add and monitor wallets.

## Discord Commands

WalletPulse includes commands for managing wallets, creating groups, checking system status, and testing alerts.

Examples:

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

WalletPulse attempts to detect:

- Buys and sells
- Large buys and sells
- Token transfers
- New token activity
- Wallet convergence
- Other recognized transactions

Detection depends on available transaction data and supported on-chain programs.

## Optional PumpPortal Integration

PumpPortal account-trade monitoring is available when `PUMPPORTAL_API_KEY` is configured.

This integration is optional.

## Security

- Keep Discord tokens, webhook URLs, RPC credentials, and API keys private.
- Do not upload `walletpulse-data.json` or other files containing sensitive information.
- Never commit secrets or private wallet data to GitHub.

## Troubleshooting

**Alerts are delayed or missing**
- Check your Solana RPC connection.
- Verify your Discord credentials and webhook.
- Use `/status` and `/latency` to inspect the system.
- Public RPC endpoints may be unreliable.

**Wallet activity is not recognized**
- Some transactions may not be fully classified.
- Detection depends on available transaction data and supported programs.

## Contributing

Bug reports, suggestions, and improvements are welcome. Open an issue or submit a pull request through the [GitHub repository](https://github.com/ryvennnnnnnnnnnnn/WalletPulse).

## Creator

Created by [@ryvennnnnnnnnnnnn](https://github.com/ryvennnnnnnnnnnnn).

## Disclaimer

WalletPulse is a monitoring tool, not financial advice. Alerts may be delayed, incomplete, or incorrectly classified. Always verify transactions independently before making trading decisions.

**WalletPulse — Know when your wallets move.**
