# Valkey

This fork can use **Valkey** in place of Redis for cache, sessions, and streams.

- Keep the existing env names: `USE_REDIS`, `REDIS_URI`, `REDIS_USERNAME`, `REDIS_PASSWORD`, and related `REDIS_*` settings.
- Optional aliases: `VALKEY_URI` / `VALKEY_URL` may be provided by the operator; point `REDIS_URI` at the Valkey endpoint (`redis://valkey:6379` works with ioredis and `@keyv/redis`).
- Image: `valkey/valkey:8` (or `valkey/valkey-bundle` if you need JSON/Search/Bloom modules).
- Local cluster scripts under `redis-config/` still call `redis-server` / `redis-cli`; `valkey-server` and `valkey-cli` are drop-in replacements if you swap the commands locally.
- Redis 7.4+ only commands are not required.
