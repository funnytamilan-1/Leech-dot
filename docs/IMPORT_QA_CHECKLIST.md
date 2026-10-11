# Import and QA checklist

This checklist must be completed before calling Leech-dot production-ready.

## Import integrity
- [ ] Import all upstream text/source files and required assets from https://github.com/abhinai2244/CBML
- [ ] Preserve upstream license, copyright notices, and author credits
- [ ] Record the upstream commit SHA used for the import
- [ ] Verify no secrets or personal credentials were copied

## Static checks
- [ ] Python compile/syntax checks across all Python files
- [ ] Dependency installation in a clean environment
- [ ] Import smoke test and startup test
- [ ] Validate configuration and produce actionable missing-setting errors
- [ ] Validate callback_data byte length (Telegram limit: 64 bytes)
- [ ] Check exception handling, async task cleanup, and resource lifecycle

## Runtime checks
- [ ] Bot startup and /start
- [ ] Inline buttons and callback routes
- [ ] Single URL/file mirror and leech
- [ ] Multi-link/batch operations, pagination, and cancellation
- [ ] Download/upload failures, retries, and cleanup
- [ ] Docker build and deployment start command
- [ ] Logs redact tokens, hashes, and session strings

## Release gate
Do not mark the project complete until every applicable check is run and results are recorded. A checklist or CI workflow alone does not prove the bot works at runtime.
