# Leech-dot

A customized Telegram mirror/leech bot project based on [CBML](https://github.com/abhinai2244/CBML).

> **Status:** Import and hardening work is in progress. Do not deploy until configuration, dependencies, and runtime checks pass.

## Credits

- **Made by:** [@Code_Dots](https://t.me/Code_Dots)
- **Partner:** [@CodeRips](https://t.me/CodeRips)
- **Upstream project:** [abhinai2244/CBML](https://github.com/abhinai2244/CBML)
- Preserve all upstream authorship, notices, and the upstream **AGPL-3.0** license when redistributing upstream-derived code.

## Planned hardening

- Validate required configuration at startup without exposing secrets in logs.
- Verify Telegram callback data stays within Telegram's 64-byte limit; reject overlong values instead of silently truncating them.
- Add automated Python syntax/import checks and dependency validation.
- Check startup scripts, Docker build, external tools, and error handling.
- Test mirror/leech download-upload flows, cancellation, cleanup, and concurrent tasks.
- Redesign the README and UI text while preserving upstream attribution.

## Setup

1. Use the project's documented Python/Docker environment.
2. Configure required values such as `BOT_TOKEN`, `OWNER_ID`, `TELEGRAM_API`, and `TELEGRAM_HASH` using environment variables or a private config file.
3. Never commit bot tokens, API hashes, session strings, passwords, or other credentials.
4. Run the available checks before deploying.

## License

Upstream CBML identifies its license as **GNU Affero General Public License v3.0 (AGPL-3.0)**. Keep the original license and copyright notices with redistributed derivative code. The original license file must be imported alongside the source.
